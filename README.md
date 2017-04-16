# api documentation for  [fibers (v1.0.15)](https://github.com/laverdet/node-fibers)  [![npm package](https://img.shields.io/npm/v/npmdoc-fibers.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fibers) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fibers.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fibers)
#### Cooperative multi-tasking for Javascript

[![NPM](https://nodei.co/npm/fibers.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fibers)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fibers/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marcel Laverdet",
        "url": "https://github.com/laverdet/"
    },
    "bugs": {
        "url": "https://github.com/laverdet/node-fibers/issues"
    },
    "dependencies": {},
    "description": "Cooperative multi-tasking for Javascript",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "22f039c8f18b856190fbbe4decf056154c1eae9c",
        "tarball": "https://registry.npmjs.org/fibers/-/fibers-1.0.15.tgz"
    },
    "engines": {
        "node": ">=0.5.2"
    },
    "gitHead": "8d7e4ffeb5151ade2ef32455080fbb2ffc226e13",
    "homepage": "https://github.com/laverdet/node-fibers",
    "keywords": [
        "fiber",
        "fibers",
        "coroutine",
        "thread",
        "async",
        "parallel",
        "worker",
        "future",
        "promise"
    ],
    "license": "MIT",
    "main": "fibers",
    "maintainers": [
        {
            "name": "laverdet"
        }
    ],
    "name": "fibers",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/laverdet/node-fibers.git"
    },
    "scripts": {
        "install": "node build.js || nodejs build.js",
        "test": "node test.js || nodejs test.js"
    },
    "version": "1.0.15"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module fibers](#apidoc.module.fibers)
1.  [function <span class="apidocSignatureSpan"></span>fibers ()](#apidoc.element.fibers.fibers)
1.  [function <span class="apidocSignatureSpan">fibers.</span>toString ()](#apidoc.element.fibers.toString)
1.  [function <span class="apidocSignatureSpan">fibers.</span>yield ()](#apidoc.element.fibers.yield)
1.  number <span class="apidocSignatureSpan">fibers.</span>fibersCreated
1.  number <span class="apidocSignatureSpan">fibers.</span>poolSize



# <a name="apidoc.module.fibers"></a>[module fibers](#apidoc.module.fibers)

#### <a name="apidoc.element.fibers.fibers"></a>[function <span class="apidocSignatureSpan"></span>fibers ()](#apidoc.element.fibers.fibers)
- description and source-code
```javascript
function Fiber() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.toString"></a>[function <span class="apidocSignatureSpan">fibers.</span>toString ()](#apidoc.element.fibers.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.yield"></a>[function <span class="apidocSignatureSpan">fibers.</span>yield ()](#apidoc.element.fibers.yield)
- description and source-code
```javascript
yield = function () { [native code] }
```
- example usage
```shell
...
var Fiber = require('fibers');

function sleep(ms) {
	var fiber = Fiber.current;
	setTimeout(function() {
		fiber.run();
	}, ms);
	Fiber.yield();
}

Fiber(function() {
	console.log('wait... ' + new Date);
	sleep(1000);
	console.log('ok... ' + new Date);
}).run();
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
