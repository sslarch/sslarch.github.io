[![Website](https://img.shields.io/website/https/sslarch.github.io.svg?maxAge=2592000)](https://sslarch.github.io/) [![GitHub contributors](https://img.shields.io/github/contributors/sslarch/sslarch.github.io.svg?maxAge=2592000)](https://github.com/sslarch/sslarch.github.io)

# CAA SSLA website

This is the source repository of <https://sslarch.github.io>, built with [hugo](https://gohugo.io/) and the [risotto theme](https://github.com/joeroe/risotto).
Contributions are welcome.
See below for instructions on how to edit the site directly, or [submit an issue](https://github.com/sslarch/sslarch.github.io/issues) to suggest a change.

## Make changes on GitHub

### Edit an existing page

You can make simple changes to the website directly on GitHub.
To edit an existing page, first find the [markdown](https://www.markdownguide.org/) source of the page you want to edit in the `content/` directory.
For example, [/documents/caa_proposal/](https://sslarch.github.io/documents/caa_proposal/) is generated from [content/documents/caa_proposal.md](https://github.com/joeroe/sslarch.github.io/blob/master/content/documents/caa_proposal.md).
Then click the edit icon to open an [edit form](https://docs.github.com/en/github/managing-files-in-a-repository/editing-files-in-your-repository) which will guide you through committing your change and submitting a pull request.

Your change will not be visible until your pull request is reviewed and accepted by the repository maintainers.

### Add a new page

To add a new page, navigate to a directory and click `Add file > Create new file` and follow the same procedure as editing an existing page.

The structure of the `content/` directory is used to organise the website: top-level pages (e.g. [/statement/](https://sslarch.github.io/statement)) are generated from an `.md` file with the same name in the root of `content/`, while those nested under a listing page (e.g. [/minutes/2019-04-24](https://sslarch.github.io/minutes/2019-04-24/)) should be created in the appropriate subdirectory.
You will probably want to copy the structure of an existing page.
At a minimum, every page needs a YAML header with a title, for example:

```markdown
---
title: "A new page"
---

Content of the **new page**, using [markdown syntax](https://www.markdownguide.org/)
```

Note that the title does not need to be repeated in the body of the page; it is automatically added when the site is built.

## Make changes locally

To preview more complex changes before submitting a pull request, [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) this repository and clone your fork **with the `--recursive` flag**:

```shell
git clone --recursive https://github.com/<username>/sslarch.github.io
```

The `--recursive` flag ensures that you also get the [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) containing the site's theme.

You will need to have [hugo installed](https://gohugo.io/getting-started/installing/) to build the site.
Use `hugo serve` to preview your changes live.

When you are finished, commit your changes and submit a pull request.
The site is automatically rebuilt when a pull request is accepted, so there is no need to use `hugo build` manually.
