# Webpack Dev Server getApp

> **THIS SERVER SHOULD BE USED FOR DEVELOPMENT ONLY!**
> **DO NOT USE IT IN PRODUCTION!**
  
## The Origin Project [webpack-dev-server](https://github.com/webpack/webpack-dev-server)
  
Current Version `2.1.0-beta.4`
  
## [Documentation](http://webpack.github.io/docs/webpack-dev-server.html)
  
##Installation
  
```
npm install webpack-dev-server-getApp --save-dev
```
  
##Enhance
  
add a option `addExtension`,it will return `app`([express](https://expressjs.com/)) and do something what you want.
  
```js
const webpack = require("webpack")
const webpackDevServer = require("webpack-dev-server-getApp")
const compiler = webpack(webpackConfig)

var bundler = new webpackDevServer(compiler, {
    contentBase: 'build',
	...
	addExtension: addExtension // Enhance ()
});
 
// add Extension 
function addExtension(app){
	// do something 
}
```

##Example

###react-router

if your project use [`react-router`](https://github.com/reactjs/react-router), you can follow as blow

```js
var bundler = new webpackDevServer(compiler, {
    ...
    addExtension: addExtension
});

/* add routing */
function addExtension(app) {
    app.get(/\/[\w-]*/, function (req, res){ 
        res.sendFile(`${process.cwd()}/build/index.html`)
    })
}
```
if you want more information about react-router please see **[Histories-browser history](https://github.com/reactjs/react-router/blob/master/docs/guides/Histories.md#browserhistory)**.

## License
Copyright 2012-2016 Tobias Koppers
[MIT](http://www.opensource.org/licenses/mit-license.php)
