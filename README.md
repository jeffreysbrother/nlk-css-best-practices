#Ninthlink CSS Best Practices

Since we have not yet settled on best practices regarding pre-processors (Sass), build tools (Gulp/Grunt), or design methodologies (like BEM), the focus of this document is *plain CSS*. The following articles serve as a decent starting-point:

* [WordPress CSS coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/)
* [Structuring CSS in large projects](https://medium.com/peergrade-io/structuring-css-in-large-projects-37f1695f5ec8#.7f42jl9ke)
* [Principles of writing consistent, idiomatic CSS](https://github.com/necolas/idiomatic-css)

###Guidelines

* Ensure that all styles accurately reflect the structure of the Table of Contents
* Only use relevant class and id names
* Be consistent with formatting
* Avoid redundant code, unnecessary overrides, and an excessive number of font sizes
* Include liberal, but not excessive, comments (aim for increased clarity...not clutter)
* Reference JIRA ticket numbers where helpful

* determine optimal text editor settings (tabs/spaces, LF/CRLF, plugin for collapsing commented sections?)
* enforce the use of rems in new projects?
* include useful defaults (font sizes, resets not included in Normalize.css like the equal height columns hack, Safari form normalization)
