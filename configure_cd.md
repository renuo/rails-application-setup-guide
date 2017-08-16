# Configure a Continuous Deployment (CD)

You can configure continuous deployment on *SemaphoreCI*.

Configure an automatic deployment to each *Heroku* application (`[project-name]-master`,`[project-name]-develop`,`[project-name]-testing`)
and execute the following script:

```shell
git push --force heroku $BRANCH_NAME:master
heroku run -x "rails db:migrate || rails db:setup"
```

this will deploy the code and migrate the database to the latest version.

Name each server with the `[branch-name]` you are deploying.