# Webpack 5 Boilerplate Template

![Maintenance](https://img.shields.io/maintenance/yes/2021?logo=github)
![webpack-current](https://img.shields.io/badge/webpack-v5.44.0-green?logo=webpack)
![node-current (scoped)](https://img.shields.io/node/v/@weareathlon/frontend-webpack-boilerplate)
[![Build Status](https://travis-ci.com/WeAreAthlon/frontend-webpack-boilerplate.svg?branch=master)](https://travis-ci.com/WeAreAthlon/frontend-webpack-boilerplate)
[![@weareathlon/frontend-webpack-boilerplate](https://snyk.io/advisor/npm-package/@weareathlon/frontend-webpack-boilerplate/badge.svg)](https://snyk.io/advisor/npm-package/@weareathlon/frontend-webpack-boilerplate)
[![GitHub Issues](https://img.shields.io/github/issues-raw/WeAreAthlon/frontend-webpack-boilerplate)](https://github.com/WeAreAthlon/frontend-webpack-boilerplate/issues)
[![Known Vulnerabilities](https://snyk.io/test/github/WeAreAthlon/frontend-webpack-boilerplate/badge.svg?targetFile=package.json)](https://snyk.io/test/github/WeAreAthlon/frontend-webpack-boilerplate?targetFile=package.json)
[![devDependency Status](https://david-dm.org/WeAreAthlon/frontend-webpack-boilerplate/dev-status.svg)](https://david-dm.org/WeAreAthlon/frontend-webpack-boilerplate?type=dev)
[![npm](https://img.shields.io/npm/dm/@weareathlon/frontend-webpack-boilerplate)](https://www.npmjs.com/package/@weareathlon/frontend-webpack-boilerplate)
[![GitHub License](https://img.shields.io/github/license/WeAreAthlon/frontend-webpack-boilerplate)](https://github.com/WeAreAthlon/frontend-webpack-boilerplate/blob/master/LICENSE)

* Demo project files to be used as a reference and **example demo** building of:
  * *JavaScript*
  * *SASS / PostCSS*
  * *HTML* templates
  * *Images* (*CSS backgrounds and image tags*)
  * *Fonts*
* Support for **assets optimization** for production environment with ability to configure:
  * **Code Minification** of *JavaScript* and *CSS* processed files.
  * **Optimize Assets Loading** - inline and embed **images** / **fonts** files having file size below a *configurable* threshold value.
  * **Images Optimisation** - optimize `jpeg`, `jpg`, `png`, `gif`, `svg` filesize and loading type via [`imagemin`](https://github.com/imagemin/imagemin). Plugin and Loader for webpack to optimize (*compress*) all images using `imagemin`. Do not worry about size of images, now they are always optimized/compressed.
* Support for **source code syntax style and formatting linters** that analyze source code to flag any programming errors, bugs, stylistic errors or suspicious constructs:
  * **SASS/PostCSS syntax cheker** - you can change or add additional rules in `.sasslintrc` file. Configuration options can be found on [`sass-lint`](https://github.com/sasstools/sass-lint/blob/master/lib/config/sass-lint.yml) documentation.
  * **JavaScript syntax checker** - following the `airbnb` style, you can review and configure the rules in `.eslintrc` file. Configuration options can be found on [`eslint`](https://eslint.org/docs/user-guide/configuring) documentation.
* Latest [Webpack 5](https://github.com/webpack/webpack) - *JavaScript* module bundler.
* Latest [SASS/PostCSS](https://github.com/sass/sass) compiler based on Dart `sass`.
* Latest [Babel 7](https://github.com/babel/babel) (`@babel/core`) - JavaScript compiler - _Use next generation JavaScript, today._
* Integration with [Travis CI](https://travis-ci.com/)
  * [Demo deployment available to GitHub pages](https://weareathlon.github.io/frontend-webpack-boilerplate/)
* Configured and ready to use **Webpack Dev Server** plugin for faster local development - [`webpack-dev-server`](https://webpack.js.org/configuration/dev-server/)
* Integration with [Webpack Bundle Analyzer](https://www.npmjs.com/package/webpack-bundle-analyzer) - _Visualize size of webpack output files with an interactive zoomable treemap._

1. Choose and download the latest template release from this repo.
2. Extract the release archive to a new directory, rename it to your project name and browse the directory.
3. Install all dependencies using `npm` *clean install* command. 

```sh 
$ npm ci
```

> More on the clean install npm command can be read here [`npm ci`](https://docs.npmjs.com/cli/ci.html)

> You can still use `npm install` in cases the `npm ci` raises system error due to specific platform incompatibilities.

# Development

## Assets Source

* **SASS/PostCSS** files are located under `src/scss/`
* **JavaScript** files with support of latest ECMAScript _ES6 / ECMAScript 2016(ES7)/ etc_ files are located under `src/js/`
* **Image** files are located under `src/images/`
* **Font** files are located under `src/fonts/`
* **HTML** files are located under `src/`
  * It will **automatically** build **all HTML files** placed under `src/` directory, no need to manually configure each template anymore!

## Build Assets

### One time build assets for development

```sh
$ npm run build
```

### Build assets and enable source files watcher

```sh
$ npm run watch
```

This command is suitable if you develop with external web server.

### Start a development server - reloading automatically after each file change.

```sh
$ npm run dev
```

# Production 

## Build Assets

Optimize assets for production by:

```sh
$ npm run production
```

## Get Built Assets

* _CSS_ files are located under `/dist/css/`
* _JavaScript_ files with support of _ES6 / ECMAScript 2016(ES7)_ files are located under `/dist/js/`
* _Images_ are located under `/dist/images/`
  * Images part of the _design_ (_usually referenced in the CSS_) are located under `/dist/images/design/`
  * Images part of the _content_ (_usually referenced via `<img>` tags_) are located under `/dist/images/content/`
* _Fonts_ are located under `/dist/fonts/`
* _HTML_ files are located under `/dist/`

# Run Code Style Linters

## SASS

```sh
$ npm run lint:sass
```
## JavaScript

```sh
$ npm run lint:js
```
