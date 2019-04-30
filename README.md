[![Website](https://img.shields.io/website/https/sslarch.github.io.svg?maxAge=2592000)](https://sslarch.github.io/) [![GitHub contributors](https://img.shields.io/github/contributors/sslarch/sslarch.github.io.svg?maxAge=2592000)](https://github.com/sslarch/sslarch.github.io)

## Website of the SIG SSLA

To learn more please see https://sslarch.github.io.

#### How it works 

This an [RMarkdown Website](http://rmarkdown.rstudio.com/rmarkdown_websites.html) based on [this](https://github.com/rstudio/rmarkdown-website) example.

- To apply changes just clone the repo, edit the relevant .Rmd files, knit the files with the <kbd>Knit HTML</kbd> button of RStudio and push the changes to the .Rmd and the .html file. That's it - no more magic involved.

- If you want to create a new subpage you also have to add it to the static part of the **_site.yml** file.

- To update everything after a change you can press the <kbd>Build All</kbd> button of RStudio or use `rmarkdown::render_site()`. This will trigger the attempt to rebuild **index.Rmd**, **statement.Rmd** and all the other .Rmd files in the repository.

- If a change does not appear online try to clear your browser cache.
