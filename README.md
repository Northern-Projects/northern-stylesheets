## Designed by Isabela Porto

## How to use

git submodule add https://github.com/Northern-Projects/northern-stylesheets.git app/assets/stylesheets

## Setup

Ensure you have bootstrap and it's dependencies

```bash
yarn add bootstrap
yarn add jquery popper.js
```

Ensure you have the following gems in your Rails `Gemfile`

```ruby
# Gemfile
gem 'autoprefixer-rails'
gem 'font-awesome-sass', '~> 5.6.1'
gem 'simple_form'
```
