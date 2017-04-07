# api documentation for  [mockjs (v1.0.0)](http://mockjs.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-mockjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mockjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mockjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mockjs)
#### 生成随机数据 & 拦截 Ajax 请求

[![NPM](https://nodei.co/npm/mockjs.png?downloads=true)](https://www.npmjs.com/package/mockjs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mockjs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mockjs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mockjs/build/apidoc.html)

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
            "name": "nuysoft",
            "email": "nuysoft@gmail.com"
        }
    ],
    "name": "mockjs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mockjs](#apidoc.module.mockjs)
1.  [function <span class="apidocSignatureSpan">mockjs.</span>heredoc (fn)](#apidoc.element.mockjs.heredoc)
1.  [function <span class="apidocSignatureSpan">mockjs.</span>mock (rurl, rtype, template)](#apidoc.element.mockjs.mock)
1.  [function <span class="apidocSignatureSpan">mockjs.</span>setup (settings)](#apidoc.element.mockjs.setup)
1.  [function <span class="apidocSignatureSpan">mockjs.</span>toJSONSchema (template, name, path)](#apidoc.element.mockjs.toJSONSchema)
1.  [function <span class="apidocSignatureSpan">mockjs.</span>valid (template, data)](#apidoc.element.mockjs.valid)
1.  object <span class="apidocSignatureSpan">mockjs.</span>Handler
1.  object <span class="apidocSignatureSpan">mockjs.</span>RE
1.  object <span class="apidocSignatureSpan">mockjs.</span>Random
1.  object <span class="apidocSignatureSpan">mockjs.</span>Random._patternLetters
1.  object <span class="apidocSignatureSpan">mockjs.</span>Util
1.  object <span class="apidocSignatureSpan">mockjs.</span>_mocked
1.  string <span class="apidocSignatureSpan">mockjs.</span>version

#### [module mockjs.Handler](#apidoc.module.mockjs.Handler)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>_all ()](#apidoc.element.mockjs.Handler._all)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>array (options)](#apidoc.element.mockjs.Handler.array)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>boolean (options)](#apidoc.element.mockjs.Handler.boolean)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>extend ()](#apidoc.element.mockjs.Handler.extend)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>function (options)](#apidoc.element.mockjs.Handler.function)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>gen (template, name, context)](#apidoc.element.mockjs.Handler.gen)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>getValueByKeyPath (key, options)](#apidoc.element.mockjs.Handler.getValueByKeyPath)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>normalizePath (pathParts)](#apidoc.element.mockjs.Handler.normalizePath)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>number (options)](#apidoc.element.mockjs.Handler.number)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>object (options)](#apidoc.element.mockjs.Handler.object)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>placeholder (placeholder, obj, templateContext, options)](#apidoc.element.mockjs.Handler.placeholder)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>regexp (options)](#apidoc.element.mockjs.Handler.regexp)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>splitPathToArray (path)](#apidoc.element.mockjs.Handler.splitPathToArray)
1.  [function <span class="apidocSignatureSpan">mockjs.Handler.</span>string (options)](#apidoc.element.mockjs.Handler.string)

#### [module mockjs.Random](#apidoc.module.mockjs.Random)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>_brandNames ()](#apidoc.element.mockjs.Random._brandNames)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>_formatDate (date, format)](#apidoc.element.mockjs.Random._formatDate)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>_goldenRatioColor (saturation, value)](#apidoc.element.mockjs.Random._goldenRatioColor)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>_randomDate (min, max)](#apidoc.element.mockjs.Random._randomDate)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>bool (min, max, cur)](#apidoc.element.mockjs.Random.bool)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>boolean (min, max, cur)](#apidoc.element.mockjs.Random.boolean)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>capitalize (word)](#apidoc.element.mockjs.Random.capitalize)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>cfirst ()](#apidoc.element.mockjs.Random.cfirst)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>char (pool)](#apidoc.element.mockjs.Random.char)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>character (pool)](#apidoc.element.mockjs.Random.character)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>city (prefix)](#apidoc.element.mockjs.Random.city)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>clast ()](#apidoc.element.mockjs.Random.clast)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>cname ()](#apidoc.element.mockjs.Random.cname)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>color (name)](#apidoc.element.mockjs.Random.color)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>county (prefix)](#apidoc.element.mockjs.Random.county)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>cparagraph (min, max)](#apidoc.element.mockjs.Random.cparagraph)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>csentence (min, max)](#apidoc.element.mockjs.Random.csentence)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>ctitle (min, max)](#apidoc.element.mockjs.Random.ctitle)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>cword (pool, min, max)](#apidoc.element.mockjs.Random.cword)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d100 ()](#apidoc.element.mockjs.Random.d100)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d12 ()](#apidoc.element.mockjs.Random.d12)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d20 ()](#apidoc.element.mockjs.Random.d20)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d4 ()](#apidoc.element.mockjs.Random.d4)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d6 ()](#apidoc.element.mockjs.Random.d6)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>d8 ()](#apidoc.element.mockjs.Random.d8)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>dataImage (size, text)](#apidoc.element.mockjs.Random.dataImage)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>date (format)](#apidoc.element.mockjs.Random.date)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>datetime (format)](#apidoc.element.mockjs.Random.datetime)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>domain (tld)](#apidoc.element.mockjs.Random.domain)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>email (domain)](#apidoc.element.mockjs.Random.email)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>extend ()](#apidoc.element.mockjs.Random.extend)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>first ()](#apidoc.element.mockjs.Random.first)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>float (min, max, dmin, dmax)](#apidoc.element.mockjs.Random.float)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>guid ()](#apidoc.element.mockjs.Random.guid)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>hex ()](#apidoc.element.mockjs.Random.hex)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>hsl ()](#apidoc.element.mockjs.Random.hsl)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>id ()](#apidoc.element.mockjs.Random.id)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>image (size, background, foreground, format, text)](#apidoc.element.mockjs.Random.image)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>img ()](#apidoc.element.mockjs.Random.img)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>inc (step)](#apidoc.element.mockjs.Random.inc)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>increment (step)](#apidoc.element.mockjs.Random.increment)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>int (min, max)](#apidoc.element.mockjs.Random.int)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>integer (min, max)](#apidoc.element.mockjs.Random.integer)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>ip ()](#apidoc.element.mockjs.Random.ip)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>last ()](#apidoc.element.mockjs.Random.last)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>lower (str)](#apidoc.element.mockjs.Random.lower)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>name (middle)](#apidoc.element.mockjs.Random.name)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>natural (min, max)](#apidoc.element.mockjs.Random.natural)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>now (unit, format)](#apidoc.element.mockjs.Random.now)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>order (array)](#apidoc.element.mockjs.Random.order)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>paragraph (min, max)](#apidoc.element.mockjs.Random.paragraph)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>pick (arr, min, max)](#apidoc.element.mockjs.Random.pick)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>protocol ()](#apidoc.element.mockjs.Random.protocol)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>province ()](#apidoc.element.mockjs.Random.province)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>range (start, stop, step)](#apidoc.element.mockjs.Random.range)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>region ()](#apidoc.element.mockjs.Random.region)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>rgb ()](#apidoc.element.mockjs.Random.rgb)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>rgba ()](#apidoc.element.mockjs.Random.rgba)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>sentence (min, max)](#apidoc.element.mockjs.Random.sentence)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>shuffle (arr, min, max)](#apidoc.element.mockjs.Random.shuffle)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>str ()](#apidoc.element.mockjs.Random.str)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>string (pool, min, max)](#apidoc.element.mockjs.Random.string)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>time (format)](#apidoc.element.mockjs.Random.time)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>title (min, max)](#apidoc.element.mockjs.Random.title)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>tld ()](#apidoc.element.mockjs.Random.tld)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>upper (str)](#apidoc.element.mockjs.Random.upper)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>url (protocol, host)](#apidoc.element.mockjs.Random.url)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>uuid ()](#apidoc.element.mockjs.Random.uuid)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>word (min, max)](#apidoc.element.mockjs.Random.word)
1.  [function <span class="apidocSignatureSpan">mockjs.Random.</span>zip (len)](#apidoc.element.mockjs.Random.zip)
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_adSize
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_brandColors
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_patternLetters
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_rformat
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_screenSize
1.  object <span class="apidocSignatureSpan">mockjs.Random.</span>_videoSize

#### [module mockjs.Random._patternLetters](#apidoc.module.mockjs.Random._patternLetters)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>A (date)](#apidoc.element.mockjs.Random._patternLetters.A)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>HH (date)](#apidoc.element.mockjs.Random._patternLetters.HH)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>M (date)](#apidoc.element.mockjs.Random._patternLetters.M)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>MM (date)](#apidoc.element.mockjs.Random._patternLetters.MM)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>SS (date)](#apidoc.element.mockjs.Random._patternLetters.SS)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>a (date)](#apidoc.element.mockjs.Random._patternLetters.a)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>dd (date)](#apidoc.element.mockjs.Random._patternLetters.dd)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>h (date)](#apidoc.element.mockjs.Random._patternLetters.h)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>hh (date)](#apidoc.element.mockjs.Random._patternLetters.hh)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>mm (date)](#apidoc.element.mockjs.Random._patternLetters.mm)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>ss (date)](#apidoc.element.mockjs.Random._patternLetters.ss)
1.  [function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>yy (date)](#apidoc.element.mockjs.Random._patternLetters.yy)
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>H
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>S
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>T
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>d
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>m
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>s
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>y
1.  string <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>yyyy

#### [module mockjs.Util](#apidoc.module.mockjs.Util)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>each (obj, iterator, context)](#apidoc.element.mockjs.Util.each)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>extend ()](#apidoc.element.mockjs.Util.extend)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>heredoc (fn)](#apidoc.element.mockjs.Util.heredoc)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isArray (obj)](#apidoc.element.mockjs.Util.isArray)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isFunction (obj)](#apidoc.element.mockjs.Util.isFunction)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isNumeric (value)](#apidoc.element.mockjs.Util.isNumeric)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isObject (obj)](#apidoc.element.mockjs.Util.isObject)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isObjectOrArray (value)](#apidoc.element.mockjs.Util.isObjectOrArray)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isRegExp (obj)](#apidoc.element.mockjs.Util.isRegExp)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>isString (obj)](#apidoc.element.mockjs.Util.isString)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>keys (obj)](#apidoc.element.mockjs.Util.keys)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>noop ()](#apidoc.element.mockjs.Util.noop)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>type (obj)](#apidoc.element.mockjs.Util.type)
1.  [function <span class="apidocSignatureSpan">mockjs.Util.</span>values (obj)](#apidoc.element.mockjs.Util.values)



# <a name="apidoc.module.mockjs"></a>[module mockjs](#apidoc.module.mockjs)

#### <a name="apidoc.element.mockjs.heredoc"></a>[function <span class="apidocSignatureSpan">mockjs.</span>heredoc (fn)](#apidoc.element.mockjs.heredoc)
- description and source-code
```javascript
function heredoc(fn) {
	    // 1. 移除起始的 function(){ /*!
	    // 2. 移除末尾的 */ }
	    // 3. 移除起始和末尾的空格
	    return fn.toString()
	        .replace(/^[^\/]+\/\*!?/, '')
	        .replace(/\*\/[^\/]+$/, '')
	        .replace(/^[\s\xA0]+/, '').replace(/[\s\xA0]+$/, '') // .trim()
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.mock"></a>[function <span class="apidocSignatureSpan">mockjs.</span>mock (rurl, rtype, template)](#apidoc.element.mockjs.mock)
- description and source-code
```javascript
mock = function (rurl, rtype, template) {
	    // Mock.mock(template)
	    if (arguments.length === 1) {
	        return Handler.gen(rurl)
	    }
	    // Mock.mock(rurl, template)
	    if (arguments.length === 2) {
	        template = rtype
	        rtype = undefined
	    }
	    // 拦截 XHR
	    if (XHR) window.XMLHttpRequest = XHR
	    Mock._mocked[rurl + (rtype || '')] = {
	        rurl: rurl,
	        rtype: rtype,
	        template: template
	    }
	    return Mock
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.setup"></a>[function <span class="apidocSignatureSpan">mockjs.</span>setup (settings)](#apidoc.element.mockjs.setup)
- description and source-code
```javascript
setup = function (settings) {
	        return XHR.setup(settings)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.toJSONSchema"></a>[function <span class="apidocSignatureSpan">mockjs.</span>toJSONSchema (template, name, path)](#apidoc.element.mockjs.toJSONSchema)
- description and source-code
```javascript
function toJSONSchema(template, name, path) {
	    // type rule properties items
	    path = path || []
	    var result = {
	        name: typeof name === 'string' ? name.replace(Constant.RE_KEY, '$1') : name,
	        template: template,
	        type: Util.type(template), // 可能不准确，例如 { 'name|1': [{}, {} ...] }
	        rule: Parser.parse(name)
	    }
	    result.path = path.slice(0)
	    result.path.push(name === undefined ? 'ROOT' : result.name)

	    switch (result.type) {
	        case 'array':
	            result.items = []
	            Util.each(template, function(value, index) {
	                result.items.push(
	                    toJSONSchema(value, index, result.path)
	                )
	            })
	            break
	        case 'object':
	            result.properties = []
	            Util.each(template, function(value, name) {
	                result.properties.push(
	                    toJSONSchema(value, name, result.path)
	                )
	            })
	            break
	    }

	    return result

	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.valid"></a>[function <span class="apidocSignatureSpan">mockjs.</span>valid (template, data)](#apidoc.element.mockjs.valid)
- description and source-code
```javascript
function valid(template, data) {
	    var schema = toJSONSchema(template)
	    var result = Diff.diff(schema, data)
	    for (var i = 0; i < result.length; i++) {
	        // console.log(Assert.message(result[i]))
	    }
	    return result
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mockjs.Handler"></a>[module mockjs.Handler](#apidoc.module.mockjs.Handler)

#### <a name="apidoc.element.mockjs.Handler._all"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>_all ()](#apidoc.element.mockjs.Handler._all)
- description and source-code
```javascript
_all = function () {
	        var re = {};
	        for (var key in Random) re[key.toLowerCase()] = key
	        return re
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.array"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>array (options)](#apidoc.element.mockjs.Handler.array)
- description and source-code
```javascript
array = function (options) {
	        var result = [],
	            i, ii;

	        // 'name|1': []
	        // 'name|count': []
	        // 'name|min-max': []
	        if (options.template.length === 0) return result

	        // 'arr': [{ 'email': '@EMAIL' }, { 'email': '@EMAIL' }]
	        if (!options.rule.parameters) {
	            for (i = 0; i < options.template.length; i++) {
	                options.context.path.push(i)
	                options.context.templatePath.push(i)
	                result.push(
	                    Handler.gen(options.template[i], i, {
	                        path: options.context.path,
	                        templatePath: options.context.templatePath,
	                        currentContext: result,
	                        templateCurrentContext: options.template,
	                        root: options.context.root || result,
	                        templateRoot: options.context.templateRoot || options.template
	                    })
	                )
	                options.context.path.pop()
	                options.context.templatePath.pop()
	            }
	        } else {
	            // 'method|1': ['GET', 'POST', 'HEAD', 'DELETE']
	            if (options.rule.min === 1 && options.rule.max === undefined) {
	                // fix #17
	                options.context.path.push(options.name)
	                options.context.templatePath.push(options.name)
	                result = Random.pick(
	                    Handler.gen(options.template, undefined, {
	                        path: options.context.path,
	                        templatePath: options.context.templatePath,
	                        currentContext: result,
	                        templateCurrentContext: options.template,
	                        root: options.context.root || result,
	                        templateRoot: options.context.templateRoot || options.template
	                    })
	                )
	                options.context.path.pop()
	                options.context.templatePath.pop()
	            } else {
	                // 'data|+1': [{}, {}]
	                if (options.rule.parameters[2]) {
	                    options.template.__order_index = options.template.__order_index || 0

	                    options.context.path.push(options.name)
	                    options.context.templatePath.push(options.name)
	                    result = Handler.gen(options.template, undefined, {
	                        path: options.context.path,
	                        templatePath: options.context.templatePath,
	                        currentContext: result,
	                        templateCurrentContext: options.template,
	                        root: options.context.root || result,
	                        templateRoot: options.context.templateRoot || options.template
	                    })[
	                        options.template.__order_index % options.template.length
	                    ]

	                    options.template.__order_index += +options.rule.parameters[2]

	                    options.context.path.pop()
	                    options.context.templatePath.pop()

	                } else {
	                    // 'data|1-10': [{}]
	                    for (i = 0; i < options.rule.count; i++) {
	                        // 'data|1-10': [{}, {}]
	                        for (ii = 0; ii < options.template.length; ii++) {
	                            options.context.path.push(result.length)
	                            options.context.templatePath.push(ii)
	                            result.push(
	                                Handler.gen(options.template[ii], result.length, {
	                                    path: options.context.path,
	                                    templatePath: options.context.templatePath,
	                                    currentContext: result,
	                                    templateCurrentContext: options.template,
	                                    root: options.context.root || result,
	                                    templateRoo ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.boolean"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>boolean (options)](#apidoc.element.mockjs.Handler.boolean)
- description and source-code
```javascript
boolean = function (options) {
	        var result;
	        // 'prop|multiple': false, 当前值是相反值的概率倍数
	        // 'prop|probability-probability': false, 当前值与相反值的概率
	        result = options.rule.parameters ? Random.bool(options.rule.min, options.rule.max, options.template) : options.template
	        return result
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.extend"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>extend ()](#apidoc.element.mockjs.Handler.extend)
- description and source-code
```javascript
function extend() {
	    var target = arguments[0] || {},
	        i = 1,
	        length = arguments.length,
	        options, name, src, copy, clone

	    if (length === 1) {
	        target = this
	        i = 0
	    }

	    for (; i < length; i++) {
	        options = arguments[i]
	        if (!options) continue

	        for (name in options) {
	            src = target[name]
	            copy = options[name]

	            if (target === copy) continue
	            if (copy === undefined) continue

	            if (Util.isArray(copy) || Util.isObject(copy)) {
	                if (Util.isArray(copy)) clone = src && Util.isArray(src) ? src : []
	                if (Util.isObject(copy)) clone = src && Util.isObject(src) ? src : {}

	                target[name] = Util.extend(clone, copy)
	            } else {
	                target[name] = copy
	            }
	        }
	    }

	    return target
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.function"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>function (options)](#apidoc.element.mockjs.Handler.function)
- description and source-code
```javascript
function = function (options) {
	        // ( context, options )
	        return options.template.call(options.context.currentContext, options)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.gen"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>gen (template, name, context)](#apidoc.element.mockjs.Handler.gen)
- description and source-code
```javascript
gen = function (template, name, context) {
	<span class="apidocCodeCommentSpan">    /* jshint -W041 */
</span>	    name = name == undefined ? '' : (name + '')

	    context = context || {}
	    context = {
	            // 当前访问路径，只有属性名，不包括生成规则
	            path: context.path || [Constant.GUID],
	            templatePath: context.templatePath || [Constant.GUID++],
	            // 最终属性值的上下文
	            currentContext: context.currentContext,
	            // 属性值模板的上下文
	            templateCurrentContext: context.templateCurrentContext || template,
	            // 最终值的根
	            root: context.root || context.currentContext,
	            // 模板的根
	            templateRoot: context.templateRoot || context.templateCurrentContext || template
	        }
	        // console.log('path:', context.path.join('.'), template)

	    var rule = Parser.parse(name)
	    var type = Util.type(template)
	    var data

	    if (Handler[type]) {
	        data = Handler[type]({
	            // 属性值类型
	            type: type,
	            // 属性值模板
	            template: template,
	            // 属性名 + 生成规则
	            name: name,
	            // 属性名
	            parsedName: name ? name.replace(Constant.RE_KEY, '$1') : name,

	            // 解析后的生成规则
	            rule: rule,
	            // 相关上下文
	            context: context
	        })

	        if (!context.root) context.root = data
	        return data
	    }

	    return template
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.getValueByKeyPath"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>getValueByKeyPath (key, options)](#apidoc.element.mockjs.Handler.getValueByKeyPath)
- description and source-code
```javascript
getValueByKeyPath = function (key, options) {
	        var originalKey = key
	        var keyPathParts = this.splitPathToArray(key)
	        var absolutePathParts = []

	        // 绝对路径
	        if (key.charAt(0) === '/') {
	            absolutePathParts = [options.context.path[0]].concat(
	                this.normalizePath(keyPathParts)
	            )
	        } else {
	            // 相对路径
	            if (keyPathParts.length > 1) {
	                absolutePathParts = options.context.path.slice(0)
	                absolutePathParts.pop()
	                absolutePathParts = this.normalizePath(
	                    absolutePathParts.concat(keyPathParts)
	                )

	            }
	        }

	        key = keyPathParts[keyPathParts.length - 1]
	        var currentContext = options.context.root
	        var templateCurrentContext = options.context.templateRoot
	        for (var i = 1; i < absolutePathParts.length - 1; i++) {
	            currentContext = currentContext[absolutePathParts[i]]
	            templateCurrentContext = templateCurrentContext[absolutePathParts[i]]
	        }
	        // 引用的值已经计算好
	        if (currentContext && (key in currentContext)) return currentContext[key]

	        // 尚未计算，递归引用数据模板中的属性
	        if (templateCurrentContext &&
	            (typeof templateCurrentContext === 'object') &&
	            (key in templateCurrentContext) &&
	            (originalKey !== templateCurrentContext[key]) // fix #15 避免自己依赖自己
	        ) {
	            // 先计算被引用的属性值
	            templateCurrentContext[key] = Handler.gen(templateCurrentContext[key], key, {
	                currentContext: currentContext,
	                templateCurrentContext: templateCurrentContext
	            })
	            return templateCurrentContext[key]
	        }
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.normalizePath"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>normalizePath (pathParts)](#apidoc.element.mockjs.Handler.normalizePath)
- description and source-code
```javascript
normalizePath = function (pathParts) {
	        var newPathParts = []
	        for (var i = 0; i < pathParts.length; i++) {
	            switch (pathParts[i]) {
	                case '..':
	                    newPathParts.pop()
	                    break
	                case '.':
	                    break
	                default:
	                    newPathParts.push(pathParts[i])
	            }
	        }
	        return newPathParts
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.number"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>number (options)](#apidoc.element.mockjs.Handler.number)
- description and source-code
```javascript
number = function (options) {
	        var result, parts;
	        if (options.rule.decimal) { // float
	            options.template += ''
	            parts = options.template.split('.')
	                // 'float1|.1-10': 10,
	                // 'float2|1-100.1-10': 1,
	                // 'float3|999.1-10': 1,
	                // 'float4|.3-10': 123.123,
	            parts[0] = options.rule.range ? options.rule.count : parts[0]
	            parts[1] = (parts[1] || '').slice(0, options.rule.dcount)
	            while (parts[1].length < options.rule.dcount) {
	                parts[1] += (
	                    // 最后一位不能为 0：如果最后一位为 0，会被 JS 引擎忽略掉。
	                    (parts[1].length < options.rule.dcount - 1) ? Random.character('number') : Random.character('123456789')
	                )
	            }
	            result = parseFloat(parts.join('.'), 10)
	        } else { // integer
	            // 'grade1|1-100': 1,
	            result = options.rule.range && !options.rule.parameters[2] ? options.rule.count : options.template
	        }
	        return result
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.object"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>object (options)](#apidoc.element.mockjs.Handler.object)
- description and source-code
```javascript
object = function (options) {
	        var result = {},
	            keys, fnKeys, key, parsedKey, inc, i;

	        // 'obj|min-max': {}
	<span class="apidocCodeCommentSpan">        /* jshint -W041 */
</span>	        if (options.rule.min != undefined) {
	            keys = Util.keys(options.template)
	            keys = Random.shuffle(keys)
	            keys = keys.slice(0, options.rule.count)
	            for (i = 0; i < keys.length; i++) {
	                key = keys[i]
	                parsedKey = key.replace(Constant.RE_KEY, '$1')
	                options.context.path.push(parsedKey)
	                options.context.templatePath.push(key)
	                result[parsedKey] = Handler.gen(options.template[key], key, {
	                    path: options.context.path,
	                    templatePath: options.context.templatePath,
	                    currentContext: result,
	                    templateCurrentContext: options.template,
	                    root: options.context.root || result,
	                    templateRoot: options.context.templateRoot || options.template
	                })
	                options.context.path.pop()
	                options.context.templatePath.pop()
	            }

	        } else {
	            // 'obj': {}
	            keys = []
	            fnKeys = [] // #25 改变了非函数属性的顺序，查找起来不方便
	            for (key in options.template) {
	                (typeof options.template[key] === 'function' ? fnKeys : keys).push(key)
	            }
	            keys = keys.concat(fnKeys)

	            /*
	                会改变非函数属性的顺序
	                keys = Util.keys(options.template)
	                keys.sort(function(a, b) {
	                    var afn = typeof options.template[a] === 'function'
	                    var bfn = typeof options.template[b] === 'function'
	                    if (afn === bfn) return 0
	                    if (afn && !bfn) return 1
	                    if (!afn && bfn) return -1
	                })
	            */

	            for (i = 0; i < keys.length; i++) {
	                key = keys[i]
	                parsedKey = key.replace(Constant.RE_KEY, '$1')
	                options.context.path.push(parsedKey)
	                options.context.templatePath.push(key)
	                result[parsedKey] = Handler.gen(options.template[key], key, {
	                    path: options.context.path,
	                    templatePath: options.context.templatePath,
	                    currentContext: result,
	                    templateCurrentContext: options.template,
	                    root: options.context.root || result,
	                    templateRoot: options.context.templateRoot || options.template
	                })
	                options.context.path.pop()
	                options.context.templatePath.pop()
	                    // 'id|+1': 1
	                inc = key.match(Constant.RE_KEY)
	                if (inc && inc[2] && Util.type(options.template[key]) === 'number') {
	                    options.template[key] += parseInt(inc[2], 10)
	                }
	            }
	        }
	        return result
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.placeholder"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>placeholder (placeholder, obj, templateContext, options)](#apidoc.element.mockjs.Handler.placeholder)
- description and source-code
```javascript
placeholder = function (placeholder, obj, templateContext, options) {
	        // console.log(options.context.path)
	        // 1 key, 2 params
	        Constant.RE_PLACEHOLDER.exec('')
	        var parts = Constant.RE_PLACEHOLDER.exec(placeholder),
	            key = parts && parts[1],
	            lkey = key && key.toLowerCase(),
	            okey = this._all()[lkey],
	            params = parts && parts[2] || ''
	        var pathParts = this.splitPathToArray(key)

	        // 解析占位符的参数
	        try {
	            // 1. 尝试保持参数的类型
	<span class="apidocCodeCommentSpan">            /*
	                #24 [Window Firefox 30.0 引用 占位符 抛错](https://github.com/nuysoft/Mock/issues/24)
	                [BX9056: 各浏览器下 window.eval 方法的执行上下文存在差异](http://www.w3help.org/zh-cn/causes/BX9056)
	                应该属于 Window Firefox 30.0 的 BUG
	            */
</span>	            /* jshint -W061 */
	            params = eval('(function(){ return [].splice.call(arguments, 0 ) })(' + params + ')')
	        } catch (error) {
	            // 2. 如果失败，只能解析为字符串
	            // console.error(error)
	            // if (error instanceof ReferenceError) params = parts[2].split(/,\s*/);
	            // else throw error
	            params = parts[2].split(/,\s*/)
	        }

	        // 占位符优先引用数据模板中的属性
	        if (obj && (key in obj)) return obj[key]

	        // @index @key
	        // if (Constant.RE_INDEX.test(key)) return +options.name
	        // if (Constant.RE_KEY.test(key)) return options.name

	        // 绝对路径 or 相对路径
	        if (
	            key.charAt(0) === '/' ||
	            pathParts.length > 1
	        ) return this.getValueByKeyPath(key, options)

	        // 递归引用数据模板中的属性
	        if (templateContext &&
	            (typeof templateContext === 'object') &&
	            (key in templateContext) &&
	            (placeholder !== templateContext[key]) // fix #15 避免自己依赖自己
	        ) {
	            // 先计算被引用的属性值
	            templateContext[key] = Handler.gen(templateContext[key], key, {
	                currentContext: obj,
	                templateCurrentContext: templateContext
	            })
	            return templateContext[key]
	        }

	        // 如果未找到，则原样返回
	        if (!(key in Random) && !(lkey in Random) && !(okey in Random)) return placeholder

	        // 递归解析参数中的占位符
	        for (var i = 0; i < params.length; i++) {
	            Constant.RE_PLACEHOLDER.exec('')
	            if (Constant.RE_PLACEHOLDER.test(params[i])) {
	                params[i] = Handler.placeholder(params[i], obj, templateContext, options)
	            }
	        }

	        var handle = Random[key] || Random[lkey] || Random[okey]
	        switch (Util.type(handle)) {
	            case 'array':
	                // 自动从数组中取一个，例如 @areas
	                return Random.pick(handle)
	            case 'function':
	                // 执行占位符方法（大多数情况）
	                handle.options = options
	                var re = handle.apply(Random, params)
	                if (re === undefined) re = '' // 因为是在字符串中，所以默认为空字符串。
	                delete handle.options
	                return re
	        }
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.regexp"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>regexp (options)](#apidoc.element.mockjs.Handler.regexp)
- description and source-code
```javascript
regexp = function (options) {
	        // regexp.source
	        var source = options.template.source

	        // 'name|1-5': /regexp/,
	        for (var i = 0; i < options.rule.count; i++) {
	            source += options.template.source
	        }

	        return RE.Handler.gen(
	            RE.Parser.parse(
	                source
	            )
	        )
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.splitPathToArray"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>splitPathToArray (path)](#apidoc.element.mockjs.Handler.splitPathToArray)
- description and source-code
```javascript
splitPathToArray = function (path) {
	        var parts = path.split(/\/+/);
	        if (!parts[parts.length - 1]) parts = parts.slice(0, -1)
	        if (!parts[0]) parts = parts.slice(1)
	        return parts;
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Handler.string"></a>[function <span class="apidocSignatureSpan">mockjs.Handler.</span>string (options)](#apidoc.element.mockjs.Handler.string)
- description and source-code
```javascript
string = function (options) {
	        var result = '',
	            i, placeholders, ph, phed;
	        if (options.template.length) {

	            //  'foo': '★',
	<span class="apidocCodeCommentSpan">            /* jshint -W041 */
</span>	            if (options.rule.count == undefined) {
	                result += options.template
	            }

	            // 'star|1-5': '★',
	            for (i = 0; i < options.rule.count; i++) {
	                result += options.template
	            }
	            // 'email|1-10': '@EMAIL, ',
	            placeholders = result.match(Constant.RE_PLACEHOLDER) || [] // A-Z_0-9 > \w_
	            for (i = 0; i < placeholders.length; i++) {
	                ph = placeholders[i]

	                // 遇到转义斜杠，不需要解析占位符
	                if (/^\\/.test(ph)) {
	                    placeholders.splice(i--, 1)
	                    continue
	                }

	                phed = Handler.placeholder(ph, options.context.currentContext, options.context.templateCurrentContext, options)

	                // 只有一个占位符，并且没有其他字符
	                if (placeholders.length === 1 && ph === result && typeof phed !== typeof result) { //
	                    result = phed
	                    break

	                    if (Util.isNumeric(phed)) {
	                        result = parseFloat(phed, 10)
	                        break
	                    }
	                    if (/^(true|false)$/.test(phed)) {
	                        result = phed === 'true' ? true :
	                            phed === 'false' ? false :
	                            phed // 已经是布尔值
	                        break
	                    }
	                }
	                result = result.replace(ph, phed)
	            }

	        } else {
	            // 'ASCII|1-10': '',
	            // 'ASCII': '',
	            result = options.rule.range ? Random.string(options.rule.count) : options.template
	        }
	        return result
	    }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mockjs.Random"></a>[module mockjs.Random](#apidoc.module.mockjs.Random)

#### <a name="apidoc.element.mockjs.Random._brandNames"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>_brandNames ()](#apidoc.element.mockjs.Random._brandNames)
- description and source-code
```javascript
_brandNames = function () {
	        var brands = [];
	        for (var b in this._brandColors) {
	            brands.push(b)
	        }
	        return brands
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._formatDate"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>_formatDate (date, format)](#apidoc.element.mockjs.Random._formatDate)
- description and source-code
```javascript
_formatDate = function (date, format) {
	        return format.replace(this._rformat, function creatNewSubString($0, flag) {
	            return typeof patternLetters[flag] === 'function' ? patternLetters[flag](date) :
	                patternLetters[flag] in patternLetters ? creatNewSubString($0, patternLetters[flag]) :
	                date[patternLetters[flag]]()
	        })
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._goldenRatioColor"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>_goldenRatioColor (saturation, value)](#apidoc.element.mockjs.Random._goldenRatioColor)
- description and source-code
```javascript
_goldenRatioColor = function (saturation, value) {
	        this._goldenRatio = 0.618033988749895
	        this._hue = this._hue || Math.random()
	        this._hue += this._goldenRatio
	        this._hue %= 1

	        if (typeof saturation !== "number") saturation = 0.5;
	        if (typeof value !== "number") value = 0.95;

	        return [
	            this._hue * 360,
	            saturation * 100,
	            value * 100
	        ]
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._randomDate"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>_randomDate (min, max)](#apidoc.element.mockjs.Random._randomDate)
- description and source-code
```javascript
_randomDate = function (min, max) { // min, max
	        min = min === undefined ? new Date(0) : min
	        max = max === undefined ? new Date() : max
	        return new Date(Math.random() * (max.getTime() - min.getTime()))
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.bool"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>bool (min, max, cur)](#apidoc.element.mockjs.Random.bool)
- description and source-code
```javascript
bool = function (min, max, cur) {
	        return this.boolean(min, max, cur)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.boolean"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>boolean (min, max, cur)](#apidoc.element.mockjs.Random.boolean)
- description and source-code
```javascript
boolean = function (min, max, cur) {
	        if (cur !== undefined) {
	            min = typeof min !== 'undefined' && !isNaN(min) ? parseInt(min, 10) : 1
	            max = typeof max !== 'undefined' && !isNaN(max) ? parseInt(max, 10) : 1
	            return Math.random() > 1.0 / (min + max) * min ? !cur : cur
	        }

	        return Math.random() >= 0.5
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.capitalize"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>capitalize (word)](#apidoc.element.mockjs.Random.capitalize)
- description and source-code
```javascript
capitalize = function (word) {
			return (word + '').charAt(0).toUpperCase() + (word + '').substr(1)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.cfirst"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>cfirst ()](#apidoc.element.mockjs.Random.cfirst)
- description and source-code
```javascript
cfirst = function () {
			var names = (
				'王 李 张 刘 陈 杨 赵 黄 周 吴 ' +
				'徐 孙 胡 朱 高 林 何 郭 马 罗 ' +
				'梁 宋 郑 谢 韩 唐 冯 于 董 萧 ' +
				'程 曹 袁 邓 许 傅 沈 曾 彭 吕 ' +
				'苏 卢 蒋 蔡 贾 丁 魏 薛 叶 阎 ' +
				'余 潘 杜 戴 夏 锺 汪 田 任 姜 ' +
				'范 方 石 姚 谭 廖 邹 熊 金 陆 ' +
				'郝 孔 白 崔 康 毛 邱 秦 江 史 ' +
				'顾 侯 邵 孟 龙 万 段 雷 钱 汤 ' +
				'尹 黎 易 常 武 乔 贺 赖 龚 文'
			).split(' ')
			return this.pick(names)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.char"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>char (pool)](#apidoc.element.mockjs.Random.char)
- description and source-code
```javascript
char = function (pool) {
	        return this.character(pool)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.character"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>character (pool)](#apidoc.element.mockjs.Random.character)
- description and source-code
```javascript
character = function (pool) {
	        var pools = {
	            lower: 'abcdefghijklmnopqrstuvwxyz',
	            upper: 'ABCDEFGHIJKLMNOPQRSTUVWXYZ',
	            number: '0123456789',
	            symbol: '!@#$%^&*()[]'
	        }
	        pools.alpha = pools.lower + pools.upper
	        pools['undefined'] = pools.lower + pools.upper + pools.number + pools.symbol

	        pool = pools[('' + pool).toLowerCase()] || pool
	        return pool.charAt(this.natural(0, pool.length - 1))
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.city"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>city (prefix)](#apidoc.element.mockjs.Random.city)
- description and source-code
```javascript
city = function (prefix) {
	        var province = this.pick(DICT)
	        var city = this.pick(province.children)
	        return prefix ? [province.name, city.name].join(' ') : city.name
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.clast"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>clast ()](#apidoc.element.mockjs.Random.clast)
- description and source-code
```javascript
clast = function () {
			var names = (
				'伟 芳 娜 秀英 敏 静 丽 强 磊 军 ' +
				'洋 勇 艳 杰 娟 涛 明 超 秀兰 霞 ' +
				'平 刚 桂英'
			).split(' ')
			return this.pick(names)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.cname"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>cname ()](#apidoc.element.mockjs.Random.cname)
- description and source-code
```javascript
cname = function () {
			return this.cfirst() + this.clast()
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.color"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>color (name)](#apidoc.element.mockjs.Random.color)
- description and source-code
```javascript
color = function (name) {
	        if (name || DICT[name]) return DICT[name].nicer
	        return this.hex()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.county"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>county (prefix)](#apidoc.element.mockjs.Random.county)
- description and source-code
```javascript
county = function (prefix) {
	        var province = this.pick(DICT)
	        var city = this.pick(province.children)
	        var county = this.pick(city.children) || {
	            name: '-'
	        }
	        return prefix ? [province.name, city.name, county.name].join(' ') : county.name
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.cparagraph"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>cparagraph (min, max)](#apidoc.element.mockjs.Random.cparagraph)
- description and source-code
```javascript
cparagraph = function (min, max) {
	        var len = range(3, 7, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.csentence())
	        }
	        return result.join('')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.csentence"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>csentence (min, max)](#apidoc.element.mockjs.Random.csentence)
- description and source-code
```javascript
csentence = function (min, max) {
	        var len = range(12, 18, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.cword())
	        }

	        return result.join('') + '。'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.ctitle"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>ctitle (min, max)](#apidoc.element.mockjs.Random.ctitle)
- description and source-code
```javascript
ctitle = function (min, max) {
	        var len = range(3, 7, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.cword())
	        }
	        return result.join('')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.cword"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>cword (pool, min, max)](#apidoc.element.mockjs.Random.cword)
- description and source-code
```javascript
cword = function (pool, min, max) {
	        // 最常用的 500 个汉字 http://baike.baidu.com/view/568436.htm
	        var DICT_KANZI = '的一是在不了有和人这中大为上个国我以要他时来用们生到作地于出就分对成会可主发年动同工也能下过子说产种面而方后多定行学法所民得经十三之进着等部度家电力里如水化高自二理起小物现实加量都两体制机当使点从业本去把性好应开它合还因由其些然前外天政四日那社义事平形相全表间样与关各重新线内数正心反你明看原又么利比或但质气第向道命此变条只没结解问意建月公无系军很情者最立代想已通并提直题党程展五果料象员革位入常文总次品式活设及管特件长求老头基资边流路级少图山统接知较将组见计别她手角期根论运农指几九区强放决西被干做必战先回则任取据处队南给色光门即保治北造百规热领七海口东导器压志世金增争济阶油思术极交受联什认六共权收证改清己美再采转更单风切打白教速花带安场身车例真务具万每目至达走积示议声报斗完类八离华名确才科张信马节话米整空元况今集温传土许步群广石记需段研界拉林律叫且究观越织装影算低持音众书布复容儿须际商非验连断深难近矿千周委素技备半办青省列习响约支般史感劳便团往酸历市克何除消构府称太准精值号率族维划选标写存候毛亲快效斯院查江型眼王按格养易置派层片始却专状育厂京识适属圆包火住调满县局照参红细引听该铁价严龙飞'

	        var len
	        switch (arguments.length) {
	            case 0: // ()
	                pool = DICT_KANZI
	                len = 1
	                break
	            case 1: // ( pool )
	                if (typeof arguments[0] === 'string') {
	                    len = 1
	                } else {
	                    // ( length )
	                    len = pool
	                    pool = DICT_KANZI
	                }
	                break
	            case 2:
	                // ( pool, length )
	                if (typeof arguments[0] === 'string') {
	                    len = min
	                } else {
	                    // ( min, max )
	                    len = this.natural(pool, min)
	                    pool = DICT_KANZI
	                }
	                break
	            case 3:
	                len = this.natural(min, max)
	                break
	        }

	        var result = ''
	        for (var i = 0; i < len; i++) {
	            result += pool.charAt(this.natural(0, pool.length - 1))
	        }
	        return result
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d100"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d100 ()](#apidoc.element.mockjs.Random.d100)
- description and source-code
```javascript
d100 = function () {
			return this.natural(1, 100)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d12"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d12 ()](#apidoc.element.mockjs.Random.d12)
- description and source-code
```javascript
d12 = function () {
			return this.natural(1, 12)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d20"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d20 ()](#apidoc.element.mockjs.Random.d20)
- description and source-code
```javascript
d20 = function () {
			return this.natural(1, 20)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d4"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d4 ()](#apidoc.element.mockjs.Random.d4)
- description and source-code
```javascript
d4 = function () {
			return this.natural(1, 4)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d6"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d6 ()](#apidoc.element.mockjs.Random.d6)
- description and source-code
```javascript
d6 = function () {
			return this.natural(1, 6)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.d8"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>d8 ()](#apidoc.element.mockjs.Random.d8)
- description and source-code
```javascript
d8 = function () {
			return this.natural(1, 8)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.dataImage"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>dataImage (size, text)](#apidoc.element.mockjs.Random.dataImage)
- description and source-code
```javascript
dataImage = function (size, text) {
	        var canvas
	        if (typeof document !== 'undefined') {
	            canvas = document.createElement('canvas')
	        } else {
	<span class="apidocCodeCommentSpan">            /*
	                https://github.com/Automattic/node-canvas
	                    npm install canvas --save
	                安装问题：
	                * http://stackoverflow.com/questions/22953206/gulp-issues-with-cario-install-command-not-found-when-trying-to-installing
-canva
	                * https://github.com/Automattic/node-canvas/issues/415
	                * https://github.com/Automattic/node-canvas/wiki/_pages

	                PS：node-canvas 的安装过程实在是太繁琐了，所以不放入 package.json 的 dependencies。
	             */
</span>	            var Canvas = module.require('canvas')
	            canvas = new Canvas()
	        }

	        var ctx = canvas && canvas.getContext && canvas.getContext("2d")
	        if (!canvas || !ctx) return ''

	        if (!size) size = this.pick(this._adSize)
	        text = text !== undefined ? text : size

	        size = size.split('x')

	        var width = parseInt(size[0], 10),
	            height = parseInt(size[1], 10),
	            background = this._brandColors[this.pick(this._brandNames())],
	            foreground = '#FFF',
	            text_height = 14,
	            font = 'sans-serif';

	        canvas.width = width
	        canvas.height = height
	        ctx.textAlign = 'center'
	        ctx.textBaseline = 'middle'
	        ctx.fillStyle = background
	        ctx.fillRect(0, 0, width, height)
	        ctx.fillStyle = foreground
	        ctx.font = 'bold ' + text_height + 'px ' + font
	        ctx.fillText(text, (width / 2), (height / 2), width)
	        return canvas.toDataURL('image/png')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.date"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>date (format)](#apidoc.element.mockjs.Random.date)
- description and source-code
```javascript
date = function (format) {
	        format = format || 'yyyy-MM-dd'
	        return this._formatDate(this._randomDate(), format)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.datetime"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>datetime (format)](#apidoc.element.mockjs.Random.datetime)
- description and source-code
```javascript
datetime = function (format) {
	        format = format || 'yyyy-MM-dd HH:mm:ss'
	        return this._formatDate(this._randomDate(), format)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.domain"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>domain (tld)](#apidoc.element.mockjs.Random.domain)
- description and source-code
```javascript
domain = function (tld) {
	        return this.word() + '.' + (tld || this.tld())
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.email"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>email (domain)](#apidoc.element.mockjs.Random.email)
- description and source-code
```javascript
email = function (domain) {
	        return this.character('lower') + '.' + this.word() + '@' +
	            (
	                domain ||
	                (this.word() + '.' + this.tld())
	            )
	            // return this.character('lower') + '.' + this.last().toLowerCase() + '@' + this.last().toLowerCase() + '.' + this.
tld()
	            // return this.word() + '@' + (domain || this.domain())
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.extend"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>extend ()](#apidoc.element.mockjs.Random.extend)
- description and source-code
```javascript
function extend() {
	    var target = arguments[0] || {},
	        i = 1,
	        length = arguments.length,
	        options, name, src, copy, clone

	    if (length === 1) {
	        target = this
	        i = 0
	    }

	    for (; i < length; i++) {
	        options = arguments[i]
	        if (!options) continue

	        for (name in options) {
	            src = target[name]
	            copy = options[name]

	            if (target === copy) continue
	            if (copy === undefined) continue

	            if (Util.isArray(copy) || Util.isObject(copy)) {
	                if (Util.isArray(copy)) clone = src && Util.isArray(src) ? src : []
	                if (Util.isObject(copy)) clone = src && Util.isObject(src) ? src : {}

	                target[name] = Util.extend(clone, copy)
	            } else {
	                target[name] = copy
	            }
	        }
	    }

	    return target
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.first"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>first ()](#apidoc.element.mockjs.Random.first)
- description and source-code
```javascript
first = function () {
			var names = [
				// male
				"James", "John", "Robert", "Michael", "William",
				"David", "Richard", "Charles", "Joseph", "Thomas",
				"Christopher", "Daniel", "Paul", "Mark", "Donald",
				"George", "Kenneth", "Steven", "Edward", "Brian",
				"Ronald", "Anthony", "Kevin", "Jason", "Matthew",
				"Gary", "Timothy", "Jose", "Larry", "Jeffrey",
				"Frank", "Scott", "Eric"
			].concat([
				// female
				"Mary", "Patricia", "Linda", "Barbara", "Elizabeth",
				"Jennifer", "Maria", "Susan", "Margaret", "Dorothy",
				"Lisa", "Nancy", "Karen", "Betty", "Helen",
				"Sandra", "Donna", "Carol", "Ruth", "Sharon",
				"Michelle", "Laura", "Sarah", "Kimberly", "Deborah",
				"Jessica", "Shirley", "Cynthia", "Angela", "Melissa",
				"Brenda", "Amy", "Anna"
			])
			return this.pick(names)
				// or this.capitalize(this.word())
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.float"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>float (min, max, dmin, dmax)](#apidoc.element.mockjs.Random.float)
- description and source-code
```javascript
float = function (min, max, dmin, dmax) {
	        dmin = dmin === undefined ? 0 : dmin
	        dmin = Math.max(Math.min(dmin, 17), 0)
	        dmax = dmax === undefined ? 17 : dmax
	        dmax = Math.max(Math.min(dmax, 17), 0)
	        var ret = this.integer(min, max) + '.';
	        for (var i = 0, dcount = this.natural(dmin, dmax); i < dcount; i++) {
	            ret += (
	                // 最后一位不能为 0：如果最后一位为 0，会被 JS 引擎忽略掉。
	                (i < dcount - 1) ? this.character('number') : this.character('123456789')
	            )
	        }
	        return parseFloat(ret, 10)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.guid"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>guid ()](#apidoc.element.mockjs.Random.guid)
- description and source-code
```javascript
guid = function () {
			var pool = "abcdefABCDEF1234567890",
				guid = this.string(pool, 8) + '-' +
				this.string(pool, 4) + '-' +
				this.string(pool, 4) + '-' +
				this.string(pool, 4) + '-' +
				this.string(pool, 12);
			return guid
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.hex"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>hex ()](#apidoc.element.mockjs.Random.hex)
- description and source-code
```javascript
hex = function () {
	        var hsv = this._goldenRatioColor()
	        var rgb = Convert.hsv2rgb(hsv)
	        var hex = Convert.rgb2hex(rgb[0], rgb[1], rgb[2])
	        return hex
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.hsl"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>hsl ()](#apidoc.element.mockjs.Random.hsl)
- description and source-code
```javascript
hsl = function () {
	        var hsv = this._goldenRatioColor()
	        var hsl = Convert.hsv2hsl(hsv)
	        return 'hsl(' +
	            parseInt(hsl[0], 10) + ', ' +
	            parseInt(hsl[1], 10) + ', ' +
	            parseInt(hsl[2], 10) + ')'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.id"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>id ()](#apidoc.element.mockjs.Random.id)
- description and source-code
```javascript
id = function () {
			var id,
				sum = 0,
				rank = [
					"7", "9", "10", "5", "8", "4", "2", "1", "6", "3", "7", "9", "10", "5", "8", "4", "2"
				],
				last = [
					"1", "0", "X", "9", "8", "7", "6", "5", "4", "3", "2"
				]

			id = this.pick(DICT).id +
				this.date('yyyyMMdd') +
				this.string('number', 3)

			for (var i = 0; i < id.length; i++) {
				sum += id[i] * rank[i];
			}
			id += last[sum % 11];

			return id
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.image"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>image (size, background, foreground, format, text)](#apidoc.element.mockjs.Random.image)
- description and source-code
```javascript
image = function (size, background, foreground, format, text) {
	        // Random.image( size, background, foreground, text )
	        if (arguments.length === 4) {
	            text = format
	            format = undefined
	        }
	        // Random.image( size, background, text )
	        if (arguments.length === 3) {
	            text = foreground
	            foreground = undefined
	        }
	        // Random.image()
	        if (!size) size = this.pick(this._adSize)

	        if (background && ~background.indexOf('#')) background = background.slice(1)
	        if (foreground && ~foreground.indexOf('#')) foreground = foreground.slice(1)

	        // http://dummyimage.com/600x400/cc00cc/470047.png&text=hello
	        return 'http://dummyimage.com/' + size +
	            (background ? '/' + background : '') +
	            (foreground ? '/' + foreground : '') +
	            (format ? '.' + format : '') +
	            (text ? '&text=' + text : '')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.img"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>img ()](#apidoc.element.mockjs.Random.img)
- description and source-code
```javascript
img = function () {
	        return this.image.apply(this, arguments)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.inc"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>inc (step)](#apidoc.element.mockjs.Random.inc)
- description and source-code
```javascript
inc = function (step) {
			return this.increment(step)
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.increment"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>increment (step)](#apidoc.element.mockjs.Random.increment)
- description and source-code
```javascript
increment = function (step) {
				return key += (+step || 1) // step?
			}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.int"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>int (min, max)](#apidoc.element.mockjs.Random.int)
- description and source-code
```javascript
int = function (min, max) {
	        return this.integer(min, max)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.integer"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>integer (min, max)](#apidoc.element.mockjs.Random.integer)
- description and source-code
```javascript
integer = function (min, max) {
	        min = typeof min !== 'undefined' ? parseInt(min, 10) : -9007199254740992
	        max = typeof max !== 'undefined' ? parseInt(max, 10) : 9007199254740992 // 2^53
	        return Math.round(Math.random() * (max - min)) + min
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.ip"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>ip ()](#apidoc.element.mockjs.Random.ip)
- description and source-code
```javascript
ip = function () {
	        return this.natural(0, 255) + '.' +
	            this.natural(0, 255) + '.' +
	            this.natural(0, 255) + '.' +
	            this.natural(0, 255)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.last"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>last ()](#apidoc.element.mockjs.Random.last)
- description and source-code
```javascript
last = function () {
			var names = [
				"Smith", "Johnson", "Williams", "Brown", "Jones",
				"Miller", "Davis", "Garcia", "Rodriguez", "Wilson",
				"Martinez", "Anderson", "Taylor", "Thomas", "Hernandez",
				"Moore", "Martin", "Jackson", "Thompson", "White",
				"Lopez", "Lee", "Gonzalez", "Harris", "Clark",
				"Lewis", "Robinson", "Walker", "Perez", "Hall",
				"Young", "Allen"
			]
			return this.pick(names)
				// or this.capitalize(this.word())
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.lower"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>lower (str)](#apidoc.element.mockjs.Random.lower)
- description and source-code
```javascript
lower = function (str) {
			return (str + '').toLowerCase()
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.name"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>name (middle)](#apidoc.element.mockjs.Random.name)
- description and source-code
```javascript
name = function (middle) {
			return this.first() + ' ' +
				(middle ? this.first() + ' ' : '') +
				this.last()
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.natural"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>natural (min, max)](#apidoc.element.mockjs.Random.natural)
- description and source-code
```javascript
natural = function (min, max) {
	        min = typeof min !== 'undefined' ? parseInt(min, 10) : 0
	        max = typeof max !== 'undefined' ? parseInt(max, 10) : 9007199254740992 // 2^53
	        return Math.round(Math.random() * (max - min)) + min
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.now"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>now (unit, format)](#apidoc.element.mockjs.Random.now)
- description and source-code
```javascript
now = function (unit, format) {
	        // now(unit) now(format)
	        if (arguments.length === 1) {
	            // now(format)
	            if (!/year|month|day|hour|minute|second|week/.test(unit)) {
	                format = unit
	                unit = ''
	            }
	        }
	        unit = (unit || '').toLowerCase()
	        format = format || 'yyyy-MM-dd HH:mm:ss'

	        var date = new Date()

	<span class="apidocCodeCommentSpan">        /* jshint -W086 */
</span>	        // 参考自 http://momentjs.cn/docs/#/manipulating/start-of/
	        switch (unit) {
	            case 'year':
	                date.setMonth(0)
	            case 'month':
	                date.setDate(1)
	            case 'week':
	            case 'day':
	                date.setHours(0)
	            case 'hour':
	                date.setMinutes(0)
	            case 'minute':
	                date.setSeconds(0)
	            case 'second':
	                date.setMilliseconds(0)
	        }
	        switch (unit) {
	            case 'week':
	                date.setDate(date.getDate() - date.getDay())
	        }

	        return this._formatDate(date, format)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.order"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>order (array)](#apidoc.element.mockjs.Random.order)
- description and source-code
```javascript
function order(array) {
			order.cache = order.cache || {}

			if (arguments.length > 1) array = [].slice.call(arguments, 0)

			// options.context.path/templatePath
			var options = order.options
			var templatePath = options.context.templatePath.join('.')

			var cache = (
				order.cache[templatePath] = order.cache[templatePath] || {
					index: 0,
					array: array
				}
			)

			return cache.array[cache.index++ % cache.array.length]
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.paragraph"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>paragraph (min, max)](#apidoc.element.mockjs.Random.paragraph)
- description and source-code
```javascript
paragraph = function (min, max) {
	        var len = range(3, 7, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.sentence())
	        }
	        return result.join(' ')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.pick"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>pick (arr, min, max)](#apidoc.element.mockjs.Random.pick)
- description and source-code
```javascript
function pick(arr, min, max) {
			arr = arr || []
			switch (arguments.length) {
				case 1:
					return arr[this.natural(0, arr.length - 1)]
				case 2:
					max = min
						<span class="apidocCodeCommentSpan">/* falls through */
</span>				case 3:
					return this.shuffle(arr, min, max)

			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.protocol"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>protocol ()](#apidoc.element.mockjs.Random.protocol)
- description and source-code
```javascript
protocol = function () {
	        return this.pick(
	            // 协议簇
	            'http ftp gopher mailto mid cid news nntp prospero telnet rlogin tn3270 wais'.split(' ')
	        )
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.province"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>province ()](#apidoc.element.mockjs.Random.province)
- description and source-code
```javascript
province = function () {
	        return this.pick(DICT).name
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.range"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>range (start, stop, step)](#apidoc.element.mockjs.Random.range)
- description and source-code
```javascript
range = function (start, stop, step) {
	        // range( stop )
	        if (arguments.length <= 1) {
	            stop = start || 0;
	            start = 0;
	        }
	        // range( start, stop )
	        step = arguments[2] || 1;

	        start = +start
	        stop = +stop
	        step = +step

	        var len = Math.max(Math.ceil((stop - start) / step), 0);
	        var idx = 0;
	        var range = new Array(len);

	        while (idx < len) {
	            range[idx++] = start;
	            start += step;
	        }

	        return range;
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.region"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>region ()](#apidoc.element.mockjs.Random.region)
- description and source-code
```javascript
region = function () {
	        return this.pick(REGION)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.rgb"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>rgb ()](#apidoc.element.mockjs.Random.rgb)
- description and source-code
```javascript
rgb = function () {
	        var hsv = this._goldenRatioColor()
	        var rgb = Convert.hsv2rgb(hsv)
	        return 'rgb(' +
	            parseInt(rgb[0], 10) + ', ' +
	            parseInt(rgb[1], 10) + ', ' +
	            parseInt(rgb[2], 10) + ')'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.rgba"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>rgba ()](#apidoc.element.mockjs.Random.rgba)
- description and source-code
```javascript
rgba = function () {
	        var hsv = this._goldenRatioColor()
	        var rgb = Convert.hsv2rgb(hsv)
	        return 'rgba(' +
	            parseInt(rgb[0], 10) + ', ' +
	            parseInt(rgb[1], 10) + ', ' +
	            parseInt(rgb[2], 10) + ', ' +
	            Math.random().toFixed(2) + ')'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.sentence"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>sentence (min, max)](#apidoc.element.mockjs.Random.sentence)
- description and source-code
```javascript
sentence = function (min, max) {
	        var len = range(12, 18, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.word())
	        }
	        return Helper.capitalize(result.join(' ')) + '.'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.shuffle"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>shuffle (arr, min, max)](#apidoc.element.mockjs.Random.shuffle)
- description and source-code
```javascript
function shuffle(arr, min, max) {
			arr = arr || []
			var old = arr.slice(0),
				result = [],
				index = 0,
				length = old.length;
			for (var i = 0; i < length; i++) {
				index = this.natural(0, old.length - 1)
				result.push(old[index])
				old.splice(index, 1)
			}
			switch (arguments.length) {
				case 0:
				case 1:
					return result
				case 2:
					max = min
						<span class="apidocCodeCommentSpan">/* falls through */
</span>				case 3:
					min = parseInt(min, 10)
					max = parseInt(max, 10)
					return result.slice(0, this.natural(min, max))
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.str"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>str ()](#apidoc.element.mockjs.Random.str)
- description and source-code
```javascript
str = function () {
	        return this.string.apply(this, arguments)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.string"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>string (pool, min, max)](#apidoc.element.mockjs.Random.string)
- description and source-code
```javascript
string = function (pool, min, max) {
	        var len
	        switch (arguments.length) {
	            case 0: // ()
	                len = this.natural(3, 7)
	                break
	            case 1: // ( length )
	                len = pool
	                pool = undefined
	                break
	            case 2:
	                // ( pool, length )
	                if (typeof arguments[0] === 'string') {
	                    len = min
	                } else {
	                    // ( min, max )
	                    len = this.natural(pool, min)
	                    pool = undefined
	                }
	                break
	            case 3:
	                len = this.natural(min, max)
	                break
	        }

	        var text = ''
	        for (var i = 0; i < len; i++) {
	            text += this.character(pool)
	        }

	        return text
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.time"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>time (format)](#apidoc.element.mockjs.Random.time)
- description and source-code
```javascript
time = function (format) {
	        format = format || 'HH:mm:ss'
	        return this._formatDate(this._randomDate(), format)
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.title"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>title (min, max)](#apidoc.element.mockjs.Random.title)
- description and source-code
```javascript
title = function (min, max) {
	        var len = range(3, 7, min, max)
	        var result = []
	        for (var i = 0; i < len; i++) {
	            result.push(this.capitalize(this.word()))
	        }
	        return result.join(' ')
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.tld"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>tld ()](#apidoc.element.mockjs.Random.tld)
- description and source-code
```javascript
tld = function () { // Top Level Domain
	        return this.pick(
	            (
	                // 域名后缀
	                'com net org edu gov int mil cn ' +
	                // 国内域名
	                'com.cn net.cn gov.cn org.cn ' +
	                // 中文国内域名
	                '中国 中国互联.公司 中国互联.网络 ' +
	                // 新国际域名
	                'tel biz cc tv info name hk mobi asia cd travel pro museum coop aero ' +
	                // 世界各国域名后缀
	                'ad ae af ag ai al am an ao aq ar as at au aw az ba bb bd be bf bg bh bi bj bm bn bo br bs bt bv bw by bz ca cc
 cf cg ch ci ck cl cm cn co cq cr cu cv cx cy cz de dj dk dm do dz ec ee eg eh es et ev fi fj fk fm fo fr ga gb gd ge gf gh gi gl
 gm gn gp gr gt gu gw gy hk hm hn hr ht hu id ie il in io iq ir is it jm jo jp ke kg kh ki km kn kp kr kw ky kz la lb lc li lk lr
 ls lt lu lv ly ma mc md mg mh ml mm mn mo mp mq mr ms mt mv mw mx my mz na nc ne nf ng ni nl no np nr nt nu nz om qa pa pe pf pg
 ph pk pl pm pn pr pt pw py re ro ru rw sa sb sc sd se sg sh si sj sk sl sm sn so sr st su sy sz tc td tf tg th tj tk tm tn to tp
 tr tt tv tw tz ua ug uk us uy va vc ve vg vn vu wf ws ye yu za zm zr zw'
	            ).split(' ')
	        )
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.upper"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>upper (str)](#apidoc.element.mockjs.Random.upper)
- description and source-code
```javascript
upper = function (str) {
			return (str + '').toUpperCase()
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.url"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>url (protocol, host)](#apidoc.element.mockjs.Random.url)
- description and source-code
```javascript
url = function (protocol, host) {
	        return (protocol || this.protocol()) + '://' + // protocol?
	            (host || this.domain()) + // host?
	            '/' + this.word()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.uuid"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>uuid ()](#apidoc.element.mockjs.Random.uuid)
- description and source-code
```javascript
uuid = function () {
			return this.guid()
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.word"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>word (min, max)](#apidoc.element.mockjs.Random.word)
- description and source-code
```javascript
word = function (min, max) {
	        var len = range(3, 10, min, max)
	        var result = '';
	        for (var i = 0; i < len; i++) {
	            result += Basic.character('lower')
	        }
	        return result
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random.zip"></a>[function <span class="apidocSignatureSpan">mockjs.Random.</span>zip (len)](#apidoc.element.mockjs.Random.zip)
- description and source-code
```javascript
zip = function (len) {
	        var zip = ''
	        for (var i = 0; i < (len || 6); i++) zip += this.natural(0, 9)
	        return zip
	    }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mockjs.Random._patternLetters"></a>[module mockjs.Random._patternLetters](#apidoc.module.mockjs.Random._patternLetters)

#### <a name="apidoc.element.mockjs.Random._patternLetters.A"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>A (date)](#apidoc.element.mockjs.Random._patternLetters.A)
- description and source-code
```javascript
A = function (date) {
	        return date.getHours() < 12 ? 'AM' : 'PM'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.HH"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>HH (date)](#apidoc.element.mockjs.Random._patternLetters.HH)
- description and source-code
```javascript
HH = function (date) {
	        var h = date.getHours()
	        return h < 10 ? '0' + h : h
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.M"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>M (date)](#apidoc.element.mockjs.Random._patternLetters.M)
- description and source-code
```javascript
M = function (date) {
	        return date.getMonth() + 1
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.MM"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>MM (date)](#apidoc.element.mockjs.Random._patternLetters.MM)
- description and source-code
```javascript
MM = function (date) {
	        var m = date.getMonth() + 1
	        return m < 10 ? '0' + m : m
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.SS"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>SS (date)](#apidoc.element.mockjs.Random._patternLetters.SS)
- description and source-code
```javascript
SS = function (date) {
	        var ms = date.getMilliseconds()
	        return ms < 10 && '00' + ms || ms < 100 && '0' + ms || ms
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.a"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>a (date)](#apidoc.element.mockjs.Random._patternLetters.a)
- description and source-code
```javascript
a = function (date) {
	        return date.getHours() < 12 ? 'am' : 'pm'
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.dd"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>dd (date)](#apidoc.element.mockjs.Random._patternLetters.dd)
- description and source-code
```javascript
dd = function (date) {
	        var d = date.getDate()
	        return d < 10 ? '0' + d : d
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.h"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>h (date)](#apidoc.element.mockjs.Random._patternLetters.h)
- description and source-code
```javascript
h = function (date) {
	        return date.getHours() % 12
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.hh"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>hh (date)](#apidoc.element.mockjs.Random._patternLetters.hh)
- description and source-code
```javascript
hh = function (date) {
	        var h = date.getHours() % 12
	        return h < 10 ? '0' + h : h
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.mm"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>mm (date)](#apidoc.element.mockjs.Random._patternLetters.mm)
- description and source-code
```javascript
mm = function (date) {
	        var m = date.getMinutes()
	        return m < 10 ? '0' + m : m
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.ss"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>ss (date)](#apidoc.element.mockjs.Random._patternLetters.ss)
- description and source-code
```javascript
ss = function (date) {
	        var s = date.getSeconds()
	        return s < 10 ? '0' + s : s
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Random._patternLetters.yy"></a>[function <span class="apidocSignatureSpan">mockjs.Random._patternLetters.</span>yy (date)](#apidoc.element.mockjs.Random._patternLetters.yy)
- description and source-code
```javascript
yy = function (date) {
	        return ('' + date.getFullYear()).slice(2)
	    }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mockjs.Util"></a>[module mockjs.Util](#apidoc.module.mockjs.Util)

#### <a name="apidoc.element.mockjs.Util.each"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>each (obj, iterator, context)](#apidoc.element.mockjs.Util.each)
- description and source-code
```javascript
function each(obj, iterator, context) {
	    var i, key
	    if (this.type(obj) === 'number') {
	        for (i = 0; i < obj; i++) {
	            iterator(i, i)
	        }
	    } else if (obj.length === +obj.length) {
	        for (i = 0; i < obj.length; i++) {
	            if (iterator.call(context, obj[i], i, obj) === false) break
	        }
	    } else {
	        for (key in obj) {
	            if (iterator.call(context, obj[key], key, obj) === false) break
	        }
	    }
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.extend"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>extend ()](#apidoc.element.mockjs.Util.extend)
- description and source-code
```javascript
function extend() {
	    var target = arguments[0] || {},
	        i = 1,
	        length = arguments.length,
	        options, name, src, copy, clone

	    if (length === 1) {
	        target = this
	        i = 0
	    }

	    for (; i < length; i++) {
	        options = arguments[i]
	        if (!options) continue

	        for (name in options) {
	            src = target[name]
	            copy = options[name]

	            if (target === copy) continue
	            if (copy === undefined) continue

	            if (Util.isArray(copy) || Util.isObject(copy)) {
	                if (Util.isArray(copy)) clone = src && Util.isArray(src) ? src : []
	                if (Util.isObject(copy)) clone = src && Util.isObject(src) ? src : {}

	                target[name] = Util.extend(clone, copy)
	            } else {
	                target[name] = copy
	            }
	        }
	    }

	    return target
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.heredoc"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>heredoc (fn)](#apidoc.element.mockjs.Util.heredoc)
- description and source-code
```javascript
function heredoc(fn) {
	    // 1. 移除起始的 function(){ /*!
	    // 2. 移除末尾的 */ }
	    // 3. 移除起始和末尾的空格
	    return fn.toString()
	        .replace(/^[^\/]+\/\*!?/, '')
	        .replace(/\*\/[^\/]+$/, '')
	        .replace(/^[\s\xA0]+/, '').replace(/[\s\xA0]+$/, '') // .trim()
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isArray"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isArray (obj)](#apidoc.element.mockjs.Util.isArray)
- description and source-code
```javascript
isArray = function (obj) {
	        return Util.type(obj) === value.toLowerCase()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isFunction"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isFunction (obj)](#apidoc.element.mockjs.Util.isFunction)
- description and source-code
```javascript
isFunction = function (obj) {
	        return Util.type(obj) === value.toLowerCase()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isNumeric"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isNumeric (value)](#apidoc.element.mockjs.Util.isNumeric)
- description and source-code
```javascript
isNumeric = function (value) {
	    return !isNaN(parseFloat(value)) && isFinite(value)
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isObject"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isObject (obj)](#apidoc.element.mockjs.Util.isObject)
- description and source-code
```javascript
isObject = function (obj) {
	        return Util.type(obj) === value.toLowerCase()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isObjectOrArray"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isObjectOrArray (value)](#apidoc.element.mockjs.Util.isObjectOrArray)
- description and source-code
```javascript
isObjectOrArray = function (value) {
	    return Util.isObject(value) || Util.isArray(value)
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isRegExp"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isRegExp (obj)](#apidoc.element.mockjs.Util.isRegExp)
- description and source-code
```javascript
isRegExp = function (obj) {
	        return Util.type(obj) === value.toLowerCase()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.isString"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>isString (obj)](#apidoc.element.mockjs.Util.isString)
- description and source-code
```javascript
isString = function (obj) {
	        return Util.type(obj) === value.toLowerCase()
	    }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.keys"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>keys (obj)](#apidoc.element.mockjs.Util.keys)
- description and source-code
```javascript
keys = function (obj) {
	    var keys = [];
	    for (var key in obj) {
	        if (obj.hasOwnProperty(key)) keys.push(key)
	    }
	    return keys;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.noop"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>noop ()](#apidoc.element.mockjs.Util.noop)
- description and source-code
```javascript
noop = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.type"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>type (obj)](#apidoc.element.mockjs.Util.type)
- description and source-code
```javascript
function type(obj) {
	    return (obj === null || obj === undefined) ? String(obj) : Object.prototype.toString.call(obj).match(/\[object (\w+)\]/)[1].
toLowerCase()
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mockjs.Util.values"></a>[function <span class="apidocSignatureSpan">mockjs.Util.</span>values (obj)](#apidoc.element.mockjs.Util.values)
- description and source-code
```javascript
values = function (obj) {
	    var values = [];
	    for (var key in obj) {
	        if (obj.hasOwnProperty(key)) values.push(obj[key])
	    }
	    return values;
	}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
