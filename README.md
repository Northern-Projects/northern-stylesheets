## Setup

Ensure you have the following gems in your Rails `Gemfile`

```ruby
# Gemfile
gem 'bootstrap-sass'
gem 'font-awesome-sass'
```

Then you can **completely replace** the `assets/stylesheets` default folder by this repo. You're done.

## Adding new `.scss` files

Look at your main `application.css.scss` file to see how SASS files are imported.

```scss
// Graphical variables
@import "config/variables";
@import "config/bootstrap_variables";

// External libraries
@import "bootstrap";
@import "font-awesome-sprockets";
@import "font-awesome";

// Your CSS
@import "layout/index";
@import "components/index";
@import "pages/index";
@import "vendor/index";
```

For every folder (**`components`**, **`layout`**, **`pages`**, **`vendor`**), there is one `_index.css.scss` partial which is responsible for importing all the other partials of its folder.

**Example 1**: Let's say you add a new `_contact.css.scss` file in **`pages`** then modify `pages/_index.css.scss` as:

```scss
// pages/_index.css.scss
@import "home";
@import "contact";
```

**Example 2**: Let's say you add a new `_sidebar.css.scss` file in **`layout`** then modify `layout/_index.css.scss` as:

```scss
// layout/_index.css.scss
@import "base";
@import "utilities";
@import "footer";
@import "navbar";
@import "sidebar";
```

## Navbar template

Our `layout/_navbar.css.scss` code works well with our home-made ERB template which you can find [here](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html.erb). Enjoy.