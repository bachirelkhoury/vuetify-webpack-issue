### Steps to reproduce
Either clone this project then run:
`npm run dev`

Or you can start fresh:

1. Start a new project: `vue init vuetifyjs/webpack-advanced my-app-project`
2. Upgrade packages using ncu to the versions below:

```
 vuetify                             ^0.15.7  →  ^0.16.1 
 babel-eslint                         ^7.1.1  →   ^8.0.1 
 eslint                              ^3.19.0  →   ^4.8.0 
 eslint-config-standard               ^6.2.1  →  ^10.2.1 
 eslint-plugin-standard               ^2.0.1  →   ^3.0.1 
 extract-text-webpack-plugin          ^2.0.0  →   ^3.0.1 
 file-loader                         ^0.11.1  →   ^1.1.5 
 optimize-css-assets-webpack-plugin   ^2.0.0  →   ^3.2.0 
 url-loader                           ^0.5.8  →   ^0.6.2 
 webpack                              ^2.6.1  →   ^3.6.0 
```
3. `npm install`
4. `npm run dev`

### Versions
Vue 2.9.1, Vuetify 0.16.1, Webpack 3.6.0

### What is expected ?
Expected to compile and run the app normally.

### What is actually happening ?
Receiving warning in console:
```
 WARNING  Compiled with 1 warnings                                                                                                                                           11:37:25 am

 warning  in ./src/main.js

7:8-15 "export 'default' (imported as 'Vuetify') was not found in 'vuetify'

> Listening at http://localhost:8080

```
and blank page in browser with following error in JS console pointing to src/mains.js:
`line 7: Vue.use(Vuetify)`

With this error in the console:
```
vue.runtime.esm.js?ff9b:4405 Uncaught TypeError: Cannot read property 'install' of undefined
    at Function.Vue.use (vue.runtime.esm.js?ff9b:4405)
    at eval (main.js?1c90:7)
    at Object.<anonymous> (app.js:1175)
    at __webpack_require__ (app.js:678)
    at fn (app.js:88)
    at Object.<anonymous> (app.js:1065)
    at __webpack_require__ (app.js:678)
    at app.js:724
    at app.js:727
```

### Reproduction Link
https://github.com/bachirelkhoury/vuetify-webpack-issue




## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
