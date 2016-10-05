# jekyll-assets-where

Demonstrating the effect of jekyll-assets on the `where` filter.

For context, we have 2 documents: one with spaces in the title, one without. Using the `where` filter, we should be able to return either of these documents:

```
{% assign doc = site.docs | where:'title','Titlewithoutspaces' | first %}

{% assign doc = site.docs | where:'title','Title with spaces' | first %}
```

## Without jekyll-assets

1) Run `bundle install` with jekyll-assets commented out:

```
source 'https://rubygems.org'
gem 'jekyll'
# gem 'jekyll-assets', group: :jekyll_plugins
```

2) Run `bundle exec jekyll serve` and visit http://localhost:4000

The `where` filter behaves as expected.

![](http://drp.mk/i/yFT9fVkL87.png)

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
