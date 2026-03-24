# Gemfile for Trade Assistant Documentation Site
source "https://rubygems.org"

# Jekyll version (GitHub Pages compatible)
gem "jekyll", "~> 3.9"

# GitHub Pages gem (includes most plugins)
gem "github-pages", group: :jekyll_plugins

# Additional Jekyll plugins for SEO
group :jekyll_plugins do
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
  gem "jekyll-feed"
end

# Windows and JRuby does not include zoneinfo files
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
