#Ninthlink Stylesheets

The following articles contain useful information regarding common best practices for authoring and maintaining stylesheets:

* [WordPress CSS coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/)
* [Structuring CSS in large projects](https://medium.com/peergrade-io/structuring-css-in-large-projects-37f1695f5ec8#.7f42jl9ke)
* [Principles of writing consistent, idiomatic CSS](https://github.com/necolas/idiomatic-css)

###Styles in general (CSS and Sass)

* Ensure that all styles accurately reflect the structure of the Table of Contents (if one exists)
* Do not use IDs for adding styles
* Class names should be meaningful
* Formatting should be consistent
* Selectors should be grouped logically
* Always use font stacks (a series of fallbacks in case the desired font becomes unavailable)
* Always specify a fallback background color when background images or gradients are used
* Avoid redundant code, unnecessary overrides, and an excessive number of font sizes
* Avoid overly-specific rules (e.g. prefer classes over IDs and avoid `!important`)
* Avoid using inline styles
* When possible, favor a CSS rule over HTML tags such as `<strong>` or `<em>` when there is no semantic benefit for the tags (for example, if an entire block of content is bold)
* Always use CSS to add uppercase styling; screen readers will often read individual letters instead of words if the source code includes content in UPPERCASE. 
* Never edit CSS libraries directly (e.g. Bootstrap, Foundation)
* Add comments only when clarity is gained; reference JIRA ticket numbers where helpful
* prefer %, em, rem, vh, vw units over px
* Determine optimal text editor settings (tabs/spaces, LF/CRLF, plugin for collapsing commented sections?)
* Aim to write code in a way that anticipates future updates
* Styles should be supported by the latest three versions of Internet Explorer, plus Chrome and Firefox.

###Sass
* use variables when possible
* avoid excessive nesting
* adhere to the structure imposed by partials (if they exist)

###WordPress Styles
* Avoid adding styles via the WordPress admin area; it is ideal for all CSS to be centrally-located and tracked by Git

###BEM (experimental: for internal use only)

The above conventions should suffice for existing projects. However, if BEM or some alternative methodology is used, we must enforce the following *additional* conventions:

* No nested selectors
* No element selectors
* Adhere to naming convention: `block__element--modifier`
* If using Sass and Bootstrap, utility classes (`col-md-12` or `img-responsive`) should be added via the `@extend` syntax in the stylesheet; this will ensure that our BEM classes remain uncluttered.
* It might also be useful to include meta information at the top of the stylesheet; a note that BEM is being used, and a brief summary of our chosen naming convention, for example.

###Not Yet Agreed Upon
* enforce the use of rems in new projects?
* include useful defaults (font sizes, resets not included in Normalize.css like the equal height columns hack, Safari form normalization)
* WP/Drupal/static HTML?
* Is a table of contents truly necessary if our stylesheets are semantic? It's even less important if we utilize .scss partials. Perhaps a TOC would only be necessary on extra-large projects that do not make use of Sass.
