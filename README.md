# nativescript-dev-webpack

A package to help with webpacking NativeScript apps.

# Ingredients

* webpack config templates.
* helper functions that place files at the correct locations before packaging apps.
* loaders and plugins for vanilla NativeScript and Angular apps.

# Usage

```sh
$ npm install --save-dev nativescript-dev-webpack
$ npm install

$ npm run start-android-bundle
or
$ npm run start-ios-bundle
```

# Documentation

For details, see the [NativeScript docs](http://docs.nativescript.org/angular/tooling/bundling-with-webpack.html).

# Note about dependencies.

The `nativescript-dev-webpack` plugin adds a few devDependencies to the project. Make sure to run either `npm install` or `yarn` after installing the plugin.
The versions of the newly added packages depend on the versions of some of your already added packages. More specifically - `tns-core-modules` and all packages from the `@angular` scope. Since version 0.4.0, nativescript-dev-webpack will automatically add the correct development dependencies, based on what you already have installed.
You can force update your `package.json` using the `update-ns-webpack` script which you can find in `PROJECT_DIR/node_modules/.bin`.
If the bundling process fails, please make sure you have the correct versions of the packages.

If you are targetting:
```
	"tns-core-modules": "^3.0.0" or "^3.0.0-rc.1" or "rc"
	"@angular/": "^4.0.0"
```
Then you should use:
```
	"nativescript-angular": "rc" or "internal-preview"
	"@ngtools/webpack": "1.3.0"
	"typescript": "~2.2.2"
```


If you are targetting:
```
	"tns-core-modules": "~2.5.0"
	"@angular/": "^4.0.0"
```
Then you should use:
```
	"nativescript-angular": "~1.5.1"
	"@ngtools/webpack": "1.2.13"
	"typescript": "~2.1.6"
```


If you are targetting:
```
	"tns-core-modules": "~2.5.0"
	"@angular/": "~2.4.0"
```
Then you should use:
```
	"nativescript-angular": "~1.4.1"
	"@ngtools/webpack": "1.2.10"
	"typescript": "~2.1.6"
```


P.S. Also please make sure you are using the same version of all `@angular/` packages, including the devDependency of `@angular/compiler-cli`.