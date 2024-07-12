# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll-theme-chirpy", "~> 7.0", ">= 7.0.1"

gem 'jekyll-compose', group: [:jekyll_plugins]

group :development do
  if Gem.win_platform?
    gem 'tzinfo-data'

    # Enable the wdm Gem to avoid polling for changes when running the local development server
    # Fix for Windows for "error: implicit declaration of function 'rb_thread_call_without_gvl' [-Wimplicit-function-declaration]"
    # $ bundle config build.wdm -- --with-cflags=-Wno-implicit-function-declaration
    gem 'wdm', '>= 0.1.1'
  end
end

group :test do
  gem "html-proofer", "~> 5.0"
end
