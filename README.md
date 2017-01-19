# dist-only

Tool to deploy only dist folder of NodeJS project to Heroku.

### ATTENTION! STILL UNDER DEVELOPMENT!

### What it does?

* it copies all content of your `dist` folder to your `dist-only` folder
* it copies your `package.json` w/o `devDependencies` section and replaces `run` script with `dist-only-run`
* it copies your `Procfile` to `dist-only` folder
* it keeps `.git` in `dist-only` folder

### Installation
```sh
$ npm install --save-dev
```
## Usage
w/o publishing on server
```
$ npm run dist-only
```
with publishing on server
```
$ npm run dist-only --deploy $YOUR_HEROKU_APP_NAME
```


License
----

MIT
