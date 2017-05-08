## BTS WEB UI

### Setting up the development environment

1. Make sure you have Node.js and npm installed
2. Install the Grunt Command Line Interface: `npm install -g grunt-cli`
3. run `npm install`
4. run `grunt watch`

This will trigger the Grunt watch task. It

1. monitors the .less files and compiles them to css every time a change is made.
2. monitors JavaScript files and runs jslint every time a change is made.

### Testing

* Run tests: `npm test`
  * This will run a test server (`testServer.js`) and execute the UI tests against it.
  * You can also run the test server alone (e.g. to aid in UI development) with `node testServer.js --standalone`.

## React

### Testing

* Run tests: `grunt mochaTest:react`

### Source mapping
All scripts are merged into one single script app.js. If you want to trace them in a browser as separated ones, follow steps:

- Google Chrome -> Inspect Element -> Sources -> app.js
- On the bottom of the script there is a comment //# sourceMappingURL=data:application/json;charset:utf-8;base64,eyJ2 ...
- copy from "data:" to the end of line
- right click -> add Source map -> Go