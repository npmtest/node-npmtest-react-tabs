# npmtest-react-tabs

#### basic test coverage for  [react-tabs (v0.8.3)](https://github.com/reactjs/react-tabs)  [![npm package](https://img.shields.io/npm/v/npmtest-react-tabs.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-react-tabs) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-react-tabs.svg)](https://travis-ci.org/npmtest/node-npmtest-react-tabs)

#### React tabs component

[![NPM](https://nodei.co/npm/react-tabs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-tabs)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-react-tabs/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-tabs/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-react-tabs/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-react-tabs/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-react-tabs/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-react-tabs/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-react-tabs/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-react-tabs/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-react-tabs/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-tabs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-react-tabs/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-react-tabs/build/test-report.html](https://npmtest.github.io/node-npmtest-react-tabs/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-react-tabs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-react-tabs/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-react-tabs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-tabs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-tabs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-tabs/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-react-tabs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-react-tabs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "react-tabs",
    "version": "0.8.3",
    "description": "React tabs component",
    "main": "lib/main.js",
    "scripts": {
        "clean": "rimraf lib",
        "build:commonjs": "babel src/ --out-dir lib/ --ignore __tests__,__mocks__",
        "build:umd": "webpack --devtool source-map --config webpack.build.js",
        "build:umd:min": "cross-env MINIFY=1 webpack --devtool source-map --config webpack.build.js",
        "build": "npm run clean && npm run build:commonjs",
        "bundle": "mkdir -p dist && npm run build:umd && npm run build:umd:min",
        "lint": "eslint src",
        "preversion": "npm run lint && npm test && npm run build && npm run bundle && git add dist/ && git commit -m 'Publish: build bower distribution'",
        "prepublish": "npm run build",
        "test": "jest",
        "start": "webpack-dev-server --inline --content-base examples/"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/reactjs/react-tabs.git"
    },
    "author": "Matt Zabriskie",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/reactjs/react-tabs/issues"
    },
    "files": [
        "dist",
        "lib"
    ],
    "homepage": "https://github.com/reactjs/react-tabs",
    "keywords": [
        "react",
        "tabs",
        "a11y",
        "react-component"
    ],
    "peerDependencies": {
        "react": "^0.14.7 || ^15.0.0",
        "react-dom": "^0.14.7 || ^15.0.0"
    },
    "devDependencies": {
        "babel-cli": "^6.9.0",
        "babel-core": "^6.9.1",
        "babel-eslint": "^7.0.0",
        "babel-jest": "^16.0.0",
        "babel-loader": "^6.2.4",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-react": "^6.5.0",
        "babel-preset-stage-1": "^6.5.0",
        "cross-env": "^3.0.0",
        "enzyme": "^2.3.0",
        "eslint": "^2.11.1",
        "eslint-config-airbnb": "^9.0.1",
        "eslint-plugin-import": "^1.8.0",
        "eslint-plugin-jsx-a11y": "^1.2.2",
        "eslint-plugin-react": "^5.1.1",
        "jest-cli": "^16.0.0",
        "react": "^15.0.0",
        "react-addons-test-utils": "^15.0.0",
        "react-dom": "^15.0.0",
        "react-modal": "^1.3.0",
        "react-test-renderer": "^15.5.4",
        "rimraf": "^2.5.2",
        "webpack": "^1.13.1",
        "webpack-dev-server": "^1.14.1"
    },
    "dependencies": {
        "classnames": "^2.2.0",
        "create-react-class": "^15.5.2",
        "js-stylesheet": "^0.0.1",
        "prop-types": "^15.5.8"
    },
    "jest": {
        "testPathDirs": [
            "src"
        ]
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
