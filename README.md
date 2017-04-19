# npmdoc-mockjs

#### api documentation for  [mockjs (v1.0.0)](http://mockjs.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-mockjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mockjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mockjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mockjs)

#### 生成随机数据 & 拦截 Ajax 请求

[![NPM](https://nodei.co/npm/mockjs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mockjs)

- [https://npmdoc.github.io/node-npmdoc-mockjs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mockjs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mockjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mockjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mockjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mockjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "nuysoft@gmail.com"
    },
    "bin": {
        "random": "bin/random"
    },
    "bugs": {
        "url": "https://github.com/nuysoft/Mock/issues"
    },
    "dependencies": {
        "commander": "*"
    },
    "description": "生成随机数据 & 拦截 Ajax 请求",
    "devDependencies": {
        "gulp": "^3.9.0",
        "gulp-connect": "*",
        "gulp-coveralls": "^0.1.4",
        "gulp-istanbul": "^0.10.3",
        "gulp-jshint": "^2.0.0",
        "gulp-mocha": "^2.2.0",
        "gulp-mocha-phantomjs": "^0.10.1",
        "jshint": "^2.8.0",
        "jshint-stylish": "^2.1.0",
        "webpack": "^1.12.9"
    },
    "directories": {},
    "dist": {
        "shasum": "d635db53898436b109d3c5b6263eca349de02445",
        "tarball": "https://registry.npmjs.org/mockjs/-/mockjs-1.0.0.tgz"
    },
    "gitHead": "f8efc901c277f58b460c559dc490df4f6c3af979",
    "homepage": "http://mockjs.com/",
    "keywords": [
        "mock",
        "mockJSON",
        "mockAjax"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/nuysoft/Mock/blob/master/LICENSE"
        }
    ],
    "main": "./dist/mock.js",
    "maintainers": [
        {
            "name": "nuysoft"
        }
    ],
    "name": "mockjs",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/nuysoft/Mock.git"
    },
    "scripts": {
        "coveralls": "gulp coveralls",
        "test": "gulp mocha"
    },
    "spm": {
        "main": "dist/mock.js"
    },
    "title": "Mock.js",
    "version": "1.0.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
