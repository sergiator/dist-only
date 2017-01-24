# dist-only

Tool to deploy only dist folder of NodeJS project to Heroku.

### ATTENTION! STILL UNDER DEVELOPMENT!

### Installation
```sh
$ npm install -g dist-only
```
### Configuration
Run
```sh
dist-only --init
```
or add manually `dist-only-run` and `dist-only-app` commands to `scripts` section of your `package.json`
```sh
"scripts": {
    "dist-only-app": "echo \"$YOUR_HEROKU_APP_NAME\""
    "dist-only-run": "node server.bundle.js"
    ...
}
```
### Usage
Without publishing
```
$ npm run dist-only
```
With publishing
```
$ npm run dist-only --deploy
```
### Workflow

Keep in mind that you have to store your development files not in the same repo as you specified for dist-only deployment.

### Requirements

`dist-only` requires [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) to be installed on your machine.

### What it does in details?

* it copies all content of your `dist` folder into `dist-only` folder
* it copies your `package.json` w/o `devDependencies` section and replaces `run` script with `dist-only-run`
* it copies your `Procfile` to `dist-only` folder
* it keeps `.git` in `dist-only` folder related to your Heroku app
* it deploys `dist-only` folder to Heroku


License
----

MIT
