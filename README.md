#Ninthlink Stylesheets

The following articles contain useful information regarding common best practices for authoring and maintaining stylesheets:

* [WordPress CSS coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/)
* [Structuring CSS in large projects](https://medium.com/peergrade-io/structuring-css-in-large-projects-37f1695f5ec8#.7f42jl9ke)
* [Principles of writing consistent, idiomatic CSS](https://github.com/necolas/idiomatic-css)

###Styles in general (CSS and Sass)

* Ensure that all styles accurately reflect the structure of the Table of Contents (if one exists)
* Do not use IDs for adding styles
* Class names should be meaningful
* Use consistent formatting
* Avoid redundant code, unnecessary overrides, and an excessive number of font sizes
* Avoid overly-specific rules (e.g. prefer classes over IDs and avoid `!important`)
* Avoid using inline styles
* Never edit CSS libraries directly (e.g. Bootstrap, Foundation)
* Add comments only when clarity is gained; reference JIRA ticket numbers where helpful
* prefer %, em, rem, vh, vw units over px
* Determine optimal text editor settings (tabs/spaces, LF/CRLF, plugin for collapsing commented sections?)
* Aim to write code in a way that anticipates future updates

###Sass
* use variables when possible
* avoid excessive nesting
* adhere to the structure imposed by partials (if they exist)

###WordPress Styles
* Avoid adding styles via the WordPress admin area; it is ideal for all CSS to be centrally-located and tracked by Git

###BEM (or alternative methodology)

The above conventions should suffice for existing projects. If we eventually decide to make use of BEM (or some alternative methodology), we must enforce the following *additional* conventions:

* No nested selectors
* No element selectors
* Adhere to naming convention: `block__element--modifier`
* It might also be useful to include meta information at the top of the stylesheet; a note that BEM is being used, and a brief summary of our chosen naming convention, for example.

###Not Yet Agreed Upon
* enforce the use of rems in new projects?
* include useful defaults (font sizes, resets not included in Normalize.css like the equal height columns hack, Safari form normalization)
* browsers to support?
* WP/Drupal/static HTML?
* Is a table of contents truly necessary if our stylesheets are semantic? It's even less important if we utilize .scss partials. Perhaps a TOC would only be necessary on extra-large projects that do not make use of Sass.
