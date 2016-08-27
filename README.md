#Ninthlink Stylesheets

The following articles contain useful information regarding common best practices for authoring and maintaining stylesheets:

* [WordPress CSS coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/)
* [Structuring CSS in large projects](https://medium.com/peergrade-io/structuring-css-in-large-projects-37f1695f5ec8#.7f42jl9ke)
* [Principles of writing consistent, idiomatic CSS](https://github.com/necolas/idiomatic-css)

###General Guidelines (CSS and Sass)

* Ensure that all styles accurately reflect the structure of the Table of Contents
* Only use relevant .class and #id names
* Be consistent with formatting
* Avoid redundant code, unnecessary overrides, and an excessive number of font sizes
* Avoid overly-specific rules (e.g. prefer classes over IDs and avoid `!important`)
* Avoid using inline styles
* Never edit CSS libraries directly (e.g. Bootstrap, Foundation)
* Add comments only when clarity is gained
* prefer %, em, rem, vh, vw units over px
* Reference JIRA ticket numbers where helpful
* Determine optimal text editor settings (tabs/spaces, LF/CRLF, plugin for collapsing commented sections?)
* Aim to write code in a way that anticipates future updates

###Sass
* use variables when possible
* avoid excessive nesting
* adhere to the structure imposed by partials (if they exist)

###WordPress
* Avoid adding styles via the WordPress admin area; it is ideal for all CSS to be centrally-located and tracked by Git

###Not Yet Agreed Upon
* enforce the use of rems in new projects?
* include useful defaults (font sizes, resets not included in Normalize.css like the equal height columns hack, Safari form normalization)
* browsers to support?
* WP/Drupal/static HTML?
