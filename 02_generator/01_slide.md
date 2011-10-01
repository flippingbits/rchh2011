!SLIDE full-page new-chapter

# Let's get our hands dirty

!SLIDE full-page

# Create a new Mountable App

    $ rails generate plugin new app_name --full --mountable

!SLIDE full-page full-code

# App structure

    $ ls -l

      Gemfile
      Gemfile.lock
      MIT-LICENSE
      README.rdoc
      Rakefile
      app
      app_name.gemspec
      config
      db
      lib
      script
      test

!SLIDE full-page full-code

# app_name.gemspec

    Gem::Specification.new do |s|
      s.name        = "app_name"
      s.version     = AppName::VERSION
      s.authors     = ["Stefan Sprenger"]
      s.email       = ["info@stefan-sprenger.com"]
      s.homepage    = "http://www.flippingbits.org"
      s.summary     = "Here comes the summary."
      s.description = "Here comes the description."

      s.add_dependency "rails", "~> 3.1.0"

      s.add_development_dependency "sqlite3"
    end

!SLIDE full-page full-code

# lib/my\_app/engine.rb

    module AppName
      class Engine < Rails::Engine
        isolate_namespace AppName
      end
    end