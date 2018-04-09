# Ruby On Rails Prototype

So you have an idea and you want to get it running as fast as possible.
This guide is for you: it will give you hints on starting as fast as possible keeping Renuo high quality standards.
Even if is just a prototype you should follow some best practices nevertheless.

**This guide is for the setup of a prototype**.
If you have to setup a project for a client please follow the [Ruby On Rails](../ruby_on_rails/README.md) guide.

1. [Initialise the Rails App](../ruby_on_rails/app_initialisation.md)
1. [Push to Git Repository](../ruby_on_rails/first_git_push.md)
1. If you want, you can configure a CI, following this guide and taking in consideration that you have only the master
branch: [Configure the CI](../ruby_on_rails/configure_ci.md)
1. [Push to Heroku](push_to_heroku.md)
1. If you want, you can configure a CD, following this guide and taking in consideration that you have only the master
branch: [Configure Continuous Deployment](../ruby_on_rails/configure_cd.md)

Once here, your app should be up and running on all three environments.

It's now time to introduce some more tools which will help you and the team to keep a high quality during the project development.

1. [Linting and automatic checks](linting_and_automatic_check.md)
1. [RSpec](rspec.md)
1. [Gems :gem:](../suggested_gems.md)
1. [Cloudflare](cloudflare.md)
1. [README](compile_readme.md)

:tada: Finally you are ready to start working on you new project! :tada:

While everyone starts working there are some more things which you should setup.
They are not optional, but the rest of the team can start working even if those are not in place yet.

1. [GetSentry](getsentry.md)
1. [NewRelic](newrelic.md)
1. [Uptime Monitor](uptime.md)
1. [Gemnasium](gemnasium.md)

Here you will find a series of chapters and guides on how to setup some of the gems we use most often and some other
useful services:

1. [Pull Requests Template](../pull_requests_template.md)
1. [Slack and Project Notifications](../slack_and_notifications.md)
1. [Send emails](send_emails.md)
1. [Sparkpost](../sparkpost.md)
1. [Devise](devise.md)
1. [Sidekiq](sidekiq.md)
1. Paperclip / Carrierwave / Renuo Upload
1. [Cucumber](cucumber.md)
1. [Amazon S3 and Cloudfront](aws.md)
1. awesome_print `gem 'awesome_print'`
1. [bootstrap](bootstrap.md)
1. devise `gem 'devise'`
1. font awesome `gem 'font-awesome-rails'`
1. goldiloader / bullet `gem 'goldiloader'`, `gem 'bullet'`
1. JQuery `gem 'jquery-rails'`
1. Rack Tracker (Google Analytics) `gem 'rack-tracker'` --> see [Google Analytics](../google_analytics.md)
1. [Typescript](https://github.com/typescript-ruby/typescript-rails)
1. Favicons
1. Setup papertrail
1. [Rack CORS](../ruby_on_rails_api/rack_cors.md)
1. SEO
    * redirect non-www to www
    * Header tags
