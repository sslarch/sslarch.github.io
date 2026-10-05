# Mastodon auto-posting for the SIG SSLA blog

## Overview

A GitHub Actions workflow announces new blog posts on Mastodon from the @CAA_SSLA account at archaeo.social. It lives in `.github/workflows/mastodon.yml` and runs alongside the existing `gh-pages.yml` deploy workflow.

## What triggers a post

The workflow runs on every push to `master` that touches `content/blog/`. It announces a post when the push turns it from unpublished into published, judged by comparing the files before and after the whole push.

- A new file with `draft: false` is announced.
- An existing file that changes from `draft: true` to `draft: false` is announced.
- A new file added with `draft: true` and flipped to `draft: false` in a later commit of the same push is announced.
- Edits to posts that were already published are not announced.
- Posts that are still drafts after the push and `_index.md` are not announced.
- Renaming a post without substantially rewriting it is not announced.

## What gets posted

```
New on the SIG SSLA blog: <title> <url> <hashtags>
```

The title comes from the `title:` front matter field. The URL is built from the filename (`content/blog/my-post.md` becomes `https://sslarch.github.io/blog/my-post/`) or, for a folder bundle, from the folder name. Mastodon generates the link preview card.

Hashtags come from the post's `tags:` front matter. Each tag becomes a CamelCase hashtag, so `open science` becomes `#OpenScience` and `DigiArchMaintainathon` stays as written. A post with no tags gets no hashtags.

```yaml
tags:
  - DigiArchMaintainathon
```

## Timing

The deploy workflow and the Mastodon workflow start at the same time. The Mastodon job polls the post's URL every 20 seconds and posts once the page returns a successful response. The job times out after 20 minutes, so a failed deploy produces no post.

## Setup

The workflow authenticates with an access token stored as the repository secret `MASTODON_TOKEN`.

1. Log in to archaeo.social as @CAA_SSLA.
2. Go to Preferences > Development > New application. Name it `blog-poster` and enable only the `write:statuses` scope.
3. Open the application and copy "Your access token". The client key and client secret are not used.
4. In the GitHub repository, go to Settings > Secrets and variables > Actions > New repository secret. Name it `MASTODON_TOKEN` and paste the token with no quotes or trailing whitespace.

## Rotating the token

Delete the `blog-poster` application under Preferences > Development, create a new one with the same scope, and replace the `MASTODON_TOKEN` secret. Do this immediately if the token leaks, since it allows posting as @CAA_SSLA.

## Known limits

- A post that sets `slug:` or `url:` in its front matter produces a wrong link, because the URL is built from the filename.
- Hashtags built from tags containing symbols such as `+` or `.` will not link correctly on Mastodon.
- The `archetypes/default.md` template has no `tags:` field. Add `tags: []` to it so authors see the field when creating a post.
- Posts use the account's default posting privacy, which should be set to public.

## Troubleshooting

Open the Actions tab and select the latest "Post new blog entries to Mastodon" run. The "Post newly published entries" step fails with exit code 22 when Mastodon rejects the request, which usually means the token is wrong or revoked. A run that ends at the 20-minute limit means the post URL never went live, so check the deploy workflow for errors.
