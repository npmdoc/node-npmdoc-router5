# npmdoc-router5

#### api documentation for  [router5 (v4.5.2)](http://router5.github.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-router5.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-router5) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-router5.svg)](https://travis-ci.org/npmdoc/node-npmdoc-router5)

#### A simple, powerful, view-agnostic, modular and extensible router

[![NPM](https://nodei.co/npm/router5.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/router5)

- [https://npmdoc.github.io/node-npmdoc-router5/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-router5/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-router5/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-router5/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-router5/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-router5/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "router5",
    "version": "4.5.2",
    "description": "A simple, powerful, view-agnostic, modular and extensible router",
    "main": "index.js",
    "jsnext:main": "dist/es/index.js",
    "scripts": {
        "clean": "babel-node scripts/clean.js",
        "build:es": "BABEL_ENV=es babel modules --out-dir dist/es",
        "build:cjs": "babel modules --out-dir ./",
        "build:umd:core": "rollup -c rollup.config.js && rollup -c rollup.config.js --uglify",
        "build:umd:browser": "rollup -c rollup.config.js --module browser",
        "build:umd:persistentParams": "rollup -c rollup.config.js --module persistentParams",
        "build:umd:listeners": "rollup -c rollup.config.js --module listeners",
        "build:umd": "npm run build:umd:core && npm run build:umd:browser && npm run build:umd:persistentParams && npm run build:umd:listeners",
        "build": "npm run clean && npm run build:cjs && npm run build:es && npm run build:umd",
        "test": "mocha --compilers js:babel-core/register --recursive --require ./tests/_helpers.js tests/**/*.js",
        "test:cover": "babel-node node_modules/.bin/isparta cover node_modules/.bin/_mocha -- --recursive --require ./tests/_helpers.js 'tests/**/*.js'",
        "clog": "conventional-changelog -p angular -i CHANGELOG.md -s",
        "lint": "eslint modules",
        "release": "./scripts/release.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/router5/router5.git"
    },
    "keywords": [
        "router",
        "routing",
        "html5",
        "functional",
        "reactive",
        "universal",
        "isomorphic"
    ],
    "author": "Thomas Roch",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/router/router5/issues"
    },
    "homepage": "http://router5.github.io",
    "dependencies": {
        "route-node": "1.8.2",
        "router5.transition-path": "4.0.1"
    },
    "devDependencies": {
        "babel-core": "~6.21.0",
        "babel-eslint": "~7.1.1",
        "babel-plugin-external-helpers": "~6.22.0",
        "babel-plugin-transform-async-to-generator": "~6.16.0",
        "babel-plugin-transform-class-properties": "~6.19.0",
        "babel-plugin-transform-export-extensions": "~6.8.0",
        "babel-plugin-transform-object-rest-spread": "~6.20.2",
        "babel-plugin-transform-runtime": "~6.15.0",
        "babel-preset-es2015": "~6.18.0",
        "babel-preset-es2015-native-modules": "~6.9.4",
        "babel-preset-es2015-rollup": "~3.0.0",
        "chai": "~3.5.0",
        "conventional-changelog": "~1.1.0",
        "coveralls": "~2.11.15",
        "del": "~2.2.2",
        "eslint": "~3.12.2",
        "install": "^0.8.4",
        "isparta": "~4.0.0",
        "jsdom": "~9.9.1",
        "mkdirp": "~0.5.1",
        "mocha": "~3.2.0",
        "mocha-lcov-reporter": "~1.2.0",
        "npm": "^4.0.5",
        "promisify-node": "~0.4.0",
        "rimraf": "~2.5.4",
        "rollup": "~0.38.2",
        "rollup-plugin-babel": "~2.7.1",
        "rollup-plugin-node-resolve": "~2.0.0",
        "rollup-plugin-uglify": "~1.0.1",
        "sinon": "~1.17.6",
        "sinon-chai": "~2.8.0",
        "yargs": "~6.5.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
