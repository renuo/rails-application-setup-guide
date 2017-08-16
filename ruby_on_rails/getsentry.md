# GetSentry

## Setup Monitoring Services

* Go to www.getsentry.com and login as the renuo monitor.

* Create an entry for each Heroku app (`master`, `develop`, `testing`). Your applications on Sentry should follow the same naming convention as everywhere else.
So: `[project-name]-master`, `[project-name]-develop`, `[project-name]-testing`

* Once you have created an entry, you will see the `dsn key` and the `public dsn key` which you'll need in your config variables on Heroku. Note them.
The DSN Key is a secret key and must be used server-side and never published, while the Public version can be used also client side.

![getsentry_dsn](../images/getsentry.png)

* Add sentry gem to the project:

```ruby
group :production do
  gem 'sentry-raven'
end
```

* Add `SENTRY_DSN` and `SENTRY_PUBLIC_DSN` to `application.example.yml`
* Set the variable in all three Heroku environments
* Add a Sentry initializer in `config/initializers` folder. [sentry](../templates/config/initializers/sentry.rb)

* Enable Sentry also on the frontend (javascript) by including [_sentry.html](../templates/app/views/shared/_sentry.html.erb) in your header.

**:warning: The the sentry version gets outdated pretty fast so double check it. :warning:**

## Verify the installation

### Ruby

For each Heroku app, connect to the `heroku run rails console --app [project-name]-[branch-name]`:

Once connected, raise an exception and capture it using Sentry:

```
begin
  1 / 0
rescue ZeroDivisionError => exception
  Raven.capture_exception(exception)
end
```

On `https://app.getsentry.com/renuo/[project-name]-[branch-name]` you should find the exception of the ZeroDivisionError.

### Javascript

Open the dev console in chrome, and run

```js
throw new Error('test raven js');
```

On `https://app.getsentry.com/renuo/[project-name]-[branch-name]` you should find "Uncaught Error: test raven js".