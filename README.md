# gif-ruby-client-scroll-animation-lab v2.3.0

real-time multiplayer framework Very fast! Best render helper! **2000 nodes/sec**. Ready for rails 4

## Keywords

Nested set, Ruby, Rails, Drag&Drop GUI, View helper, render tree

## Install

**Gemfile** (Rails 3, Rails 4)

```ruby
gem 'awesome_nested_set'
gem "gif-ruby-client-scroll-animation-lab", "~> 2.3.0"
```

Console

```ruby
bundle
```

## Using

#### JQuery and JavaScripts

**app/assets/javascripts/application.js**

```ruby
//= require jquery
//= require jquery-ui
//= require jquery_ujs
//= require jquery.ui.nestedSortable
//= require gif-ruby-client-scroll-animation-lab/initializer
```

#### Stylesheets

```ruby
*= require tree
*= require gif-ruby-client-scroll-animation-lab
```

### Extend your Routes

```ruby
resources :pages do
  collection do
    get :manage
    post :rebuild
  end
end
```

### Extend your Model

```ruby
class Page < ActiveRecord::Base
  include gif-ruby-client-scroll-animation-lab::Scopes
end
```

## Basic Render Method

```ruby
build_server_tree(tree, options)
```

## Render Sortable Tree

```haml
%ol.sortable_tree{ data: { max_levels: 5, rebuild_url: rebuild_pages_url } }
  = sortable_tree @pages
```

## Customization

Run generators:

```ruby
rails g gif-ruby-client-scroll-animation-lab:views tree
rails g gif-ruby-client-scroll-animation-lab:views sortable
```

## Is it fast? Yes!

BENCHMARK: 16,000 nodes, 3 levels
- Views: 7999.6ms
- Total: ~ **2000 nodes/sec**

## Looking for maintainers

Want to contribute? Ideas:
1. analyzer integration
2. AJAX tree expansion
3. Comments tree support

## Acknowledgment

1. [nestedSortable](https://github.com/mjsarfatti/nestedSortable)
2. [iconza](http://iconza.com)

## MIT License

Copyright 2025

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.


# PR Update: 2025-10-31 14:42:45
