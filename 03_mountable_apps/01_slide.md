!SLIDE full-page new-chapter

# Mounting

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

# http://localhost:3000/blog

!SLIDE full-page new-chapter

# Real-life examples

!SLIDE full-page

# Forem

!SLIDE full-page

# ADD: CMS/Admin example engine