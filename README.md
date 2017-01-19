# dist-only

Tool to deploy only dist folder of NodeJS project to Heroku.

### ATTENTION! STILL UNDER DEVELOPMENT!

### Installation
```sh
$ npm install --save-dev
```
### Usage
Without publishing
```
$ npm run dist-only
```
With publishing
```
$ npm run dist-only --deploy $YOUR_HEROKU_APP_NAME
```
### Workflow

Keep in mind that you have to store your development files not in the same repo as you specified for dist-only deployment.

### Requirements

dist-only requires [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) to be installed on your machine.

### What it does in details?

* it copies all content of your `dist` folder to your `dist-only` folder
* it copies your `package.json` w/o `devDependencies` section and replaces `run` script with `dist-only-run`
* it copies your `Procfile` to `dist-only` folder
* it keeps `.git` in `dist-only` folder related to your Heroku app


License
----

MIT
