# webpack-dev-server

> **THIS SERVER SHOULD BE USED FOR DEVELOPMENT ONLY!**
> **DO NOT USE IT IN PRODUCTION!**

## The Origin Project [webpack-dev-server](https://github.com/webpack/webpack-dev-server)

Current Version `2.1.0-beta.4`

## [Documentation](http://webpack.github.io/docs/webpack-dev-server.html)

##Enhance

add a option `addExtension`, it will return app (express) and do what you want.

```js
const compiler = webpack(webpackConfig)

var bundler = new webpackDevServer(compiler, {
    addExtension: addExtension // Enhance ()
    contentBase: 'build',
	...
});

funcion addExtension(app){
	// do something 
}
```

## License

Copyright 2012-2016 Tobias Koppers

[MIT](http://www.opensource.org/licenses/mit-license.php)
