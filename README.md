# Ember Simple Auth/Browserify Issue Reproduction

This repo is to reproduce an issue with the Ember-CLI test runner breaking with both ember-browserify (1.1.4) and ember-simple-auth (1.0.1).

To see the issue after cloning this repo:

```
bower install
npm install
ember serve
```

To create the issue from scratch (with Ember-CLI 1.13.13):

```
ember new simple-auth-browerify-test
cd simple-auth-browerify-test
ember install ember-browserify
ember install ember-simple-auth
ember serve
```

Then visit the test page in your browser. Observe the error:

```
Uncaught Error: Could not find module `undefined` imported from `(require)`
  missingModule @ loader.js:135
  findModule @ loader.js:150
  requireModule @ loader.js:139
  s @ _prelude.js:1
  (anonymous function) @ qunit.js:12
```
