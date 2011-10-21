!SLIDE new-chapter

# Let's get our hands dirty

!SLIDE center

# Create a new Mountable App

    $ rails generate plugin new simple_blog --full --mountable

!SLIDE full-code

# App structure

    $ ls -l

      Gemfile
      Gemfile.lock
      MIT-LICENSE
      README.rdoc
      Rakefile
      app
      simple_blog.gemspec
      config
      db
      lib
      script
      test

!SLIDE center

# simple_blog.gemspec

    @@@ruby
    Gem::Specification.new do |s|
      s.name        = "simple_blog"
      s.version     = SimpleBlog::VERSION
      s.authors     = ["Stefan Sprenger"]
      s.email       = ["info@stefan-sprenger.com"]
      s.homepage    = "http://www.flippingbits.org"
      s.summary     = "Just a simple blog."
      s.description = "A simple blog without user " +
                      "authentication or admin interface."

      s.add_dependency "rails", "~> 3.1.0"

      s.add_development_dependency "sqlite3"
    end

!SLIDE center

# lib/simple\_blog/engine.rb

    @@@ruby
    module SimpleBlog
      class Engine < Rails::Engine
        isolate_namespace SimpleBlog
      end
    end

!SLIDE

# <span class="underlined">Configure</span> it like a Rails app

!SLIDE center

# Configuration

    @@@ruby
    # lib/simple_blog/engine.rb

    module SimpleBlog
      class Engine < Rails::Engine
        isolate_namespace SimpleBlog

        config.encoding = "utf-8"
      end
    end

!SLIDE

# Everything gets <span class="underlined">namespaced</span>

!SLIDE incremental

# Everything gets namespaced

* Models
* Controllers
* Helpers
* View-Templates
* Layouts
* Routes
* ...

!SLIDE center

# Generating models

    $ rails generate model Article title:string content:text

!SLIDE center

# Automatic namespacing

    @@@ruby
    # app/models/simple_blog/article.rb

    module SimpleBlog
      class Article < ActiveRecord::Base
      end
    end