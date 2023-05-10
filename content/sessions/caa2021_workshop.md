---
title: Developing R packages
sessionType: workshop
date: 2021-06-14
publishDate: 2021-05-17
conference: CAA 2021, Cyprus (Virtual)
conferenceUrl: https://2021.caaconference.org
sessionCode: S31
organisers:
- Sophie C. Schmidt
- Petr Pajdla
- Clemens Schmid
aliases: [ workshopi ]
---

**When:** 2021-06-14  
**Where:** Online

## Abstract

A growing number of researchers use the scripting language R (R Core Team 2020) for scientific data analysis. Many organise their code in scripts and functions to perform sequences of data manipulation, statistics and visualisation. Sometimes these workflows gain in complexity and it becomes feasible to outsource core components into a dedicated R package. Packages are one of the best ways to make R code reproducible as they provide a well established structure to share functions, data and their documentation with other R-users. The vast numbers of packages by diverse developers on the Comprehensive R Archive Network (CRAN) indicate their popularity in the scientific community and they could very well become a pillar of scientific progress in archaeology (Schmidt and Marwick 2020). Indeed more and more packages are also being developed by and for archaeologists (e.g. http://open-archaeo.info).

For CAA2021 we would like to offer a workshop to teach R-users how to develop R packages from their scripts. We believe that many archaeological R-users do not engage in package development as they lack training and the learning curve seems steep. We will try to fill this gap and offer a low-level introduction to R package development for users with basic R-skills.

This workshop is designed in tandem with the session “Tools for the Revolution: developing packages for scientific programming in archaeology” by the SIG SSLA.

Therefore:

- Do you use the scientific scripting language R for your analyses?
- Do you, too, now have a number of script files flying about and don’t know how to organise them?

Join us and learn how to create an R-package!

In this workshop we will focus on the main points in Hadley Wickham’s book on package development (Wickham 2020, https://r-pkgs.org) and create an example application together. Workshop attendees will get to know a structured workflow, which will aid them in organizing their personal scripts afterwards.

Basic topics will include: Package setup, function documentation and development cycle. As every package should come with example data, we will show how to implement these into a package, as well as more detailed function explanations within a vignette. Testing routines and licensing for publication, e.g. using git (Github, Gitlab or similar) will enable attendees to share their work safely.

Basic R knowledge is strongly recommended for the workshop. Software requirements will be announced to registered attendees later.

## References

R Core Team. 2020. R: A Language and Environment for Statistical Computing. Vienna, Austria: R Foundation for Statistical Computing. https://www.R-project.org/.

Schmidt, Sophie C, and Ben Marwick. 2020. “Tool-Driven Revolutions in Archaeological Science.” Journal of Computer Applications in Archaeology 3 (1): 18–32. doi:10.5334/jcaa.29.

Wickham, Hadley. 2020. R Packages. Organize, Test, Document and Share Your Code. 2nd ed. O’Reilly. https://r-pkgs.org/.
