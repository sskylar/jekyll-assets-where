# jekyll-assets-where

Demonstrating the effect of jekyll-assets on the `where` filter.

## With jekyll-assets

1) Run `bundle install` with the following Gemfile:

```
source 'https://rubygems.org'
gem 'jekyll'
gem 'jekyll-assets', group: :jekyll_plugins
```

2) Run `bundle exec jekyll serve` and visit http://localhost:4000

Notice how the `where` filter is able to find single word matches, but not multiple word matches:

![](http://drp.mk/i/Q28FC4KsS.png)

## Without jekyll-assets

1) Run `bundle install` with jekyll-assets commented out:

```
source 'https://rubygems.org'
gem 'jekyll'
# gem 'jekyll-assets', group: :jekyll_plugins
```

2) Run `bundle exec jekyll serve` and visit http://localhost:4000

The `where` filter now behaves as expected:

![](http://drp.mk/i/yFT9fVkL87.png)
