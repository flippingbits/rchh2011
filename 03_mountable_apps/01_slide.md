!SLIDE full-page new-chapter

# Mounting the app

!SLIDE full-page

# Add the dependency to Gemfile

    gem "simple_blog", :path => "~/Codes/simple_blog"

!SLIDE full-page

# Install migrations

    $ rake simple_blog:install:migrations
    $ rake db:migrate

!SLIDE full-page

# Add routes

    Railscamp::Application.routes.draw do
      mount SimpleBlog::Engine => "/blog"
    end

!SLIDE full-page

# Restart server

!SLIDE full-page

# GET [http://localhost:3000/blog](http://localhost:3000/blog)

!SLIDE full-page

# Enjoy!

!SLIDE full-page new-chapter

# Real-life examples

!SLIDE full-page

# Forem
## [https://github.com/radar/forem](https://github.com/radar/forem)

!SLIDE full-page

# Rails Admin
## [https://github.com/sferik/rails_admin](https://github.com/sferik/rails_admin)