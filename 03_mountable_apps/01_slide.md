!SLIDE full-page new-chapter

# Mounting

!SLIDE full-page

# Add the dependency to Gemfile

    gem "app_name", :path => "~/Codes/app_name"

!SLIDE full-page

# Add routes

    Railscamp::Application.routes.draw do
      mount AppName::Engine => "/app_name"
    end

!SLIDE full-page

# Enjoy!