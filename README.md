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


## Errors

1. no `noparse` specified (`npm run build`):

  > Uncaught Error: Cannot find module 'ember-data/core'
  
2. `ember-data` in `noparse` (`npm run build2`):
  
  > Uncaught ReferenceError: global is not defined 

3. `ember` and `ember-data` in `noparse` (`npm run build3`):

  > Uncaught Error: Cannot find module 'ember-data/core' 
  
  
## Related Issues

* Ember Data https://github.com/emberjs/data/issues/2196
* browserify-shim https://github.com/thlorenz/browserify-shim/issues/17  
  
