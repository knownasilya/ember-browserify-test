ember-browserify-test
=====================

Test Ember with ED and Browserify/shim

```bash
npm install
npm run build
npm start
```

The noparse version is `npm run build2`.
Both builds work fine, but when you run either, i.e. `npm start`, then you get different errors.
Adding `ember` to the noparse will create the global issue tracked [here](https://github.com/thlorenz/browserify-shim/issues/17).
