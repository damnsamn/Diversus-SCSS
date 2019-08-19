A generic Sass/SCSS file-structure with example files. Intended for use as a template for new Diversus projects.

# You'll need:
 - Some knowledge of how Sass works, its patterns and best practices.
	 - There are heaps of useful guides, just google it
	 - Good place to get started is the [official Sass Basics guide](https://sass-lang.com/guide)
- Some [method of sass compilation](https://sass-lang.com/install) (my go-to CLI tool is [dart-sass](https://github.com/sass/dart-sass/releases/latest))

# To build:	
    $ cd [repo]\styles
    $ sass --watch --style=compressed style.scss:style.css
 - `--watch` will automatically watch for changes to your sass files and automatically compile on every saved change.
 - `--style=compressed` will remove comments and whitespace from the compiled .css file. Remove this option for a more verbose compilation
 - `[input path]:[output path]` can be more direct paths, in case your file structure varies from this repository's example structure
	 - eg: `sass style.scss:..\css\style.css`

# Extras:
I'd strongly recommend the use of Bootstrap 4 as a baseline CSS framework - we've used it to much success across other projects. Bootstrap provides us with:
 - A responsive grid layout system
 - Normalised defaults to minimise cross-browser inconsistencies
 - SCSS utilities for responsive styling

I'd recommend grabbing the scss from [Bootstrap's Source Files](https://getbootstrap.com/docs/4.3/getting-started/download/) and throwing them in the **\vendor** folder.
I've included commented **@import** statements that will import only the files that are useful for the points above - there should be very minimal Bootstrap theming to override.