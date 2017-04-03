# api documentation for  [fibers (v1.0.15)](https://github.com/laverdet/node-fibers)  [![npm package](https://img.shields.io/npm/v/npmdoc-fibers.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fibers) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fibers.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fibers)
#### Cooperative multi-tasking for Javascript

[![NPM](https://nodei.co/npm/fibers.png?downloads=true)](https://www.npmjs.com/package/fibers)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-fibers_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fibers/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fibers/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marcel Laverdet",
        "email": "marcel@laverdet.com",
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
            "name": "laverdet",
            "email": "marcel.npm@laverdet.com"
        }
    ],
    "name": "fibers",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  [function <span class="apidocSignatureSpan">fibers.</span>future ()](#apidoc.element.fibers.future)
1.  [function <span class="apidocSignatureSpan">fibers.</span>yield ()](#apidoc.element.fibers.yield)
1.  number <span class="apidocSignatureSpan">fibers.</span>fibersCreated
1.  number <span class="apidocSignatureSpan">fibers.</span>poolSize
1.  object <span class="apidocSignatureSpan">fibers.</span>future.prototype

#### [module fibers.future](#apidoc.module.fibers.future)
1.  [function <span class="apidocSignatureSpan">fibers.</span>future (detach)](#apidoc.element.fibers.future.future)
1.  [function <span class="apidocSignatureSpan">fibers.future.</span>fromPromise (promise)](#apidoc.element.fibers.future.fromPromise)
1.  [function <span class="apidocSignatureSpan">fibers.future.</span>task (fn)](#apidoc.element.fibers.future.task)
1.  [function <span class="apidocSignatureSpan">fibers.future.</span>wait ()](#apidoc.element.fibers.future.wait)
1.  [function <span class="apidocSignatureSpan">fibers.future.</span>wrap (fnOrObject, multi, suffix, stop)](#apidoc.element.fibers.future.wrap)

#### [module fibers.future.prototype](#apidoc.module.fibers.future.prototype)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>detach ()](#apidoc.element.fibers.future.prototype.detach)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>get ()](#apidoc.element.fibers.future.prototype.get)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>isResolved ()](#apidoc.element.fibers.future.prototype.isResolved)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>promise ()](#apidoc.element.fibers.future.prototype.promise)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>proxy (future)](#apidoc.element.fibers.future.prototype.proxy)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>proxyErrors (futures)](#apidoc.element.fibers.future.prototype.proxyErrors)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolve (arg1, arg2)](#apidoc.element.fibers.future.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolveSuccess (cb)](#apidoc.element.fibers.future.prototype.resolveSuccess)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolver ()](#apidoc.element.fibers.future.prototype.resolver)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>return (value)](#apidoc.element.fibers.future.prototype.return)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>throw (error)](#apidoc.element.fibers.future.prototype.throw)
1.  [function <span class="apidocSignatureSpan">fibers.future.prototype.</span>wait ()](#apidoc.element.fibers.future.prototype.wait)



# <a name="apidoc.module.fibers"></a>[module fibers](#apidoc.module.fibers)

#### <a name="apidoc.element.fibers.future"></a>[function <span class="apidocSignatureSpan">fibers.</span>future ()](#apidoc.element.fibers.future)
- description and source-code
```javascript
function Future() {}
```
- example usage
```shell
...
// You can create functions which automatically run in their own fiber and
// return futures that resolve when the fiber returns (this probably sounds
// confusing.. just play with it to understand).
var calcTimerDelta = function(ms) {
	var start = new Date;
	sleep(ms).wait();
	return new Date - start;
}.future(); // <-- important!

// And futures also include node-friendly callbacks if you don't want to use
// wait()
calcTimerDelta(2000).resolve(function(err, val) {
	console.log('Set timer for 2000ms, waited '+ val+ 'ms');
});
'''
...
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



# <a name="apidoc.module.fibers.future"></a>[module fibers.future](#apidoc.module.fibers.future)

#### <a name="apidoc.element.fibers.future.future"></a>[function <span class="apidocSignatureSpan">fibers.</span>future (detach)](#apidoc.element.fibers.future.future)
- description and source-code
```javascript
future = function (detach) {
	var fn = this;
	var ret = function() {
		var future = new FiberFuture(fn, this, arguments);
		if (detach) {
			future.detach();
		}
		return future;
	};
	ret.toString = function() {
		return '<<Future '+ fn+ '.future()>>';
	};
	return ret;
}
```
- example usage
```shell
...
// You can create functions which automatically run in their own fiber and
// return futures that resolve when the fiber returns (this probably sounds
// confusing.. just play with it to understand).
var calcTimerDelta = function(ms) {
	var start = new Date;
	sleep(ms).wait();
	return new Date - start;
}.future(); // <-- important!

// And futures also include node-friendly callbacks if you don't want to use
// wait()
calcTimerDelta(2000).resolve(function(err, val) {
	console.log('Set timer for 2000ms, waited '+ val+ 'ms');
});
'''
...
```

#### <a name="apidoc.element.fibers.future.fromPromise"></a>[function <span class="apidocSignatureSpan">fibers.future.</span>fromPromise (promise)](#apidoc.element.fibers.future.fromPromise)
- description and source-code
```javascript
fromPromise = function (promise) {
	var future = new Future;
	promise.then(function(val) {
		future.return(val);
	}, function(err) {
		future.throw(err);
	});
	return future;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.future.task"></a>[function <span class="apidocSignatureSpan">fibers.future.</span>task (fn)](#apidoc.element.fibers.future.task)
- description and source-code
```javascript
task = function (fn) {
	if (arguments.length === 1) {
		return fn.future()();
	} else {
		var future = new Future, pending = arguments.length, error, values = new Array(arguments.length);
		for (var ii = 0; ii < arguments.length; ++ii) {
			arguments[ii].future()().resolve(function(ii, err, val) {
				if (err) {
					error = err;
				}
				values[ii] = val;
				if (--pending === 0) {
					if (error) {
						future.throw(error);
					} else {
						future.return(values);
					}
				}
			}.bind(null, ii));
		}
		return future;
	}
}
```
- example usage
```shell
...

	$ cat ls.js

'''javascript
var Future = require('fibers/future');
var fs = Future.wrap(require('fs'));

Future.task(function() {
	// Get a list of files in the directory
	var fileNames = fs.readdirFuture('.').wait();
	console.log('Found '+ fileNames.length+ ' files');

	// Stat each file
	var stats = [];
	for (var ii = 0; ii < fileNames.length; ++ii) {
...
```

#### <a name="apidoc.element.fibers.future.wait"></a>[function <span class="apidocSignatureSpan">fibers.future.</span>wait ()](#apidoc.element.fibers.future.wait)
- description and source-code
```javascript
function wait() {

	// Normalize arguments + pull out a FiberFuture for reuse if possible
	var futures = [], singleFiberFuture;
	for (var ii = 0; ii < arguments.length; ++ii) {
		var arg = arguments[ii];
		if (arg instanceof Future) {
			// Ignore already resolved fibers
			if (arg.isResolved()) {
				continue;
			}
			// Look for fiber reuse
			if (!singleFiberFuture && arg instanceof FiberFuture && !arg.started) {
				singleFiberFuture = arg;
				continue;
			}
			futures.push(arg);
		} else if (arg instanceof Array) {
			for (var jj = 0; jj < arg.length; ++jj) {
				var aarg = arg[jj];
				if (aarg instanceof Future) {
					// Ignore already resolved fibers
					if (aarg.isResolved()) {
						continue;
					}
					// Look for fiber reuse
					if (!singleFiberFuture && aarg instanceof FiberFuture && !aarg.started) {
						singleFiberFuture = aarg;
						continue;
					}
					futures.push(aarg);
				} else {
					throw new Error(aarg+ ' is not a future');
				}
			}
		} else {
			throw new Error(arg+ ' is not a future');
		}
	}

	// Resumes current fiber
	var fiber = Fiber.current;
	if (!fiber) {
		throw new Error('Can\'t wait without a fiber');
	}

	// Resolve all futures
	var pending = futures.length + (singleFiberFuture ? 1 : 0);
	function cb() {
		if (!--pending) {
			fiber.run();
		}
	}
	for (var ii = 0; ii < futures.length; ++ii) {
		futures[ii].resolve(cb);
	}

	// Reusing a fiber?
	if (singleFiberFuture) {
		singleFiberFuture.started = true;
		try {
			singleFiberFuture.return(
				singleFiberFuture.fn.apply(singleFiberFuture.context, singleFiberFuture.args));
		} catch(e) {
			singleFiberFuture.throw(e);
		}
		--pending;
	}

	// Yield this fiber
	if (pending) {
		Fiber.yield();
	}
}
```
- example usage
```shell
...

'''javascript
var Future = require('fibers/future');
var fs = Future.wrap(require('fs'));

Future.task(function() {
	// Get a list of files in the directory
	var fileNames = fs.readdirFuture('.').wait();
	console.log('Found '+ fileNames.length+ ' files');

	// Stat each file
	var stats = [];
	for (var ii = 0; ii < fileNames.length; ++ii) {
		stats.push(fs.statFuture(fileNames[ii]));
	}
...
```

#### <a name="apidoc.element.fibers.future.wrap"></a>[function <span class="apidocSignatureSpan">fibers.future.</span>wrap (fnOrObject, multi, suffix, stop)](#apidoc.element.fibers.future.wrap)
- description and source-code
```javascript
wrap = function (fnOrObject, multi, suffix, stop) {
	if (typeof fnOrObject === 'object') {
		var wrapped = Object.create(fnOrObject);
		for (var ii in fnOrObject) {
			if (wrapped[ii] instanceof Function) {
				wrapped[suffix === undefined ? ii+ 'Future' : ii+ suffix] = Future.wrap(wrapped[ii], multi, suffix, stop);
			}
		}
		return wrapped;
	} else if (typeof fnOrObject === 'function') {
		var fn = function() {
			var future = new Future;
			var args = Array.prototype.slice.call(arguments);
			if (multi) {
				var cb = future.resolver();
				args.push(function(err) {
					cb(err, Array.prototype.slice.call(arguments, 1));
				});
			} else {
				args.push(future.resolver());
			}
			future._ = fnOrObject.apply(this, args);
			return future;
		}
		// Modules like 'request' return a function that has more functions as properties. Handle this
		// in some kind of reasonable way.
		if (!stop) {
			var proto = Object.create(fnOrObject);
			for (var ii in fnOrObject) {
				if (fnOrObject.hasOwnProperty(ii) && fnOrObject[ii] instanceof Function) {
					proto[ii] = proto[ii];
				}
			}
			fn.__proto__ = Future.wrap(proto, multi, suffix, true);
		}
		return fn;
	}
}
```
- example usage
```shell
...
Using 'Future' to wrap existing node functions. At no point is the node event
loop blocked:

	$ cat ls.js

'''javascript
var Future = require('fibers/future');
var fs = Future.wrap(require('fs'));

Future.task(function() {
	// Get a list of files in the directory
	var fileNames = fs.readdirFuture('.').wait();
	console.log('Found '+ fileNames.length+ ' files');

	// Stat each file
...
```



# <a name="apidoc.module.fibers.future.prototype"></a>[module fibers.future.prototype](#apidoc.module.fibers.future.prototype)

#### <a name="apidoc.element.fibers.future.prototype.detach"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>detach ()](#apidoc.element.fibers.future.prototype.detach)
- description and source-code
```javascript
detach = function () {
		this.resolve(function(err) {
			if (err) {
				throw err;
			}
		});
	}
```
- example usage
```shell
...
		f.wait()
	});

	// Print file size
	for (var ii = 0; ii < fileNames.length; ++ii) {
		console.log(fileNames[ii]+ ': '+ stats[ii].get().size);
	}
}).detach();
'''

	$ node ls.js
	Found 11 files
	bin: 4096
	fibers.js: 1708
	.gitignore: 37
...
```

#### <a name="apidoc.element.fibers.future.prototype.get"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>get ()](#apidoc.element.fibers.future.prototype.get)
- description and source-code
```javascript
get = function () {
		if (!this.resolved) {
			throw new Error('Future must resolve before value is ready');
		} else if (this.error) {
			// Link the stack traces up
			var error = this.error;
			var localStack = {};
			Error.captureStackTrace(localStack, Future.prototype.get);
			var futureStack = Object.getOwnPropertyDescriptor(error, 'futureStack');
			if (!futureStack) {
				futureStack = Object.getOwnPropertyDescriptor(error, 'stack');
				if (futureStack) {
					Object.defineProperty(error, 'futureStack', futureStack);
				}
			}
			if (futureStack && futureStack.get) {
				Object.defineProperty(error, 'stack', {
					get: function() {
						var stack = futureStack.get.apply(error);
						if (stack) {
							stack = stack.split('\n');
							return [stack[0]]
								.concat(localStack.stack.split('\n').slice(1))
								.concat('    - - - - -')
								.concat(stack.slice(1))
								.join('\n');
						} else {
							return localStack.stack;
						}
					},
					set: function(stack) {
						Object.defineProperty(error, 'stack', {
							value: stack,
							configurable: true,
							enumerable: false,
							writable: true,
						});
					},
					configurable: true,
					enumerable: false,
				});
			}
			throw error;
		} else {
			return this.value;
		}
	}
```
- example usage
```shell
...
	}
	stats.map(function(f) {
		f.wait()
	});

	// Print file size
	for (var ii = 0; ii < fileNames.length; ++ii) {
		console.log(fileNames[ii]+ ': '+ stats[ii].get().size);
	}
}).detach();
'''

	$ node ls.js
	Found 11 files
	bin: 4096
...
```

#### <a name="apidoc.element.fibers.future.prototype.isResolved"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>isResolved ()](#apidoc.element.fibers.future.prototype.isResolved)
- description and source-code
```javascript
isResolved = function () {
		return this.resolved === true;
	}
```
- example usage
```shell
...

	// Normalize arguments + pull out a FiberFuture for reuse if possible
	var futures = [], singleFiberFuture;
	for (var ii = 0; ii < arguments.length; ++ii) {
		var arg = arguments[ii];
		if (arg instanceof Future) {
			// Ignore already resolved fibers
			if (arg.isResolved()) {
				continue;
			}
			// Look for fiber reuse
			if (!singleFiberFuture && arg instanceof FiberFuture && !arg.started) {
				singleFiberFuture = arg;
				continue;
			}
...
```

#### <a name="apidoc.element.fibers.future.prototype.promise"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>promise ()](#apidoc.element.fibers.future.prototype.promise)
- description and source-code
```javascript
promise = function () {
		var that = this;
		return new Promise(function(resolve, reject) {
			that.resolve(function(err, val) {
				if (err) {
					reject(err);
				} else {
					resolve(val);
				}
			});
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.future.prototype.proxy"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>proxy (future)](#apidoc.element.fibers.future.prototype.proxy)
- description and source-code
```javascript
proxy = function (future) {
		this.resolve(function(err, val) {
			if (err) {
				future.throw(err);
			} else {
				future.return(val);
			}
		});
	}
```
- example usage
```shell
...
* of error, and the second is a function(val){} callback.
*/
Future.prototype.resolve = function(/* errback or future, callback */) { ... }

/**
* Propogate results to another future.
*
* Example usage: future1.proxy(future2) // future2 gets automatically resolved with however future1 resolves
*/
Future.prototype.proxy = function(future) { ... }

/**
* Differs from its functional counterpart in that it actually resolves the future. Thus if the
* future threw, future.wait() will throw.
*/
...
```

#### <a name="apidoc.element.fibers.future.prototype.proxyErrors"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>proxyErrors (futures)](#apidoc.element.fibers.future.prototype.proxyErrors)
- description and source-code
```javascript
proxyErrors = function (futures) {
		this.resolve(function(err) {
			if (!err) {
				return;
			}
			if (futures instanceof Array) {
				for (var ii = 0; ii < futures.length; ++ii) {
					futures[ii].throw(err);
				}
			} else {
				futures.throw(err);
			}
		});
		return this;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.future.prototype.resolve"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolve (arg1, arg2)](#apidoc.element.fibers.future.prototype.resolve)
- description and source-code
```javascript
resolve = function (arg1, arg2) {
		if (this.resolved) {
			if (arg2) {
				if (this.error) {
					arg1.throw(this.error);
				} else {
					arg2(this.value);
				}
			} else {
				arg1(this.error, this.value);
			}
		} else {
			(this.callbacks = this.callbacks || []).push([arg1, arg2]);
		}
		return this;
	}
```
- example usage
```shell
...
	var start = new Date;
	sleep(ms).wait();
	return new Date - start;
}.future(); // <-- important!

// And futures also include node-friendly callbacks if you don't want to use
// wait()
calcTimerDelta(2000).resolve(function(err, val) {
	console.log('Set timer for 2000ms, waited '+ val+ 'ms');
});
'''

	$ node sleep.js
	Set timer for 2000ms, waited 2009ms
...
```

#### <a name="apidoc.element.fibers.future.prototype.resolveSuccess"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolveSuccess (cb)](#apidoc.element.fibers.future.prototype.resolveSuccess)
- description and source-code
```javascript
resolveSuccess = function (cb) {
		this.resolve(function(err, val) {
			if (err) {
				return;
			}
			cb(val);
		});
		return this;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fibers.future.prototype.resolver"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>resolver ()](#apidoc.element.fibers.future.prototype.resolver)
- description and source-code
```javascript
resolver = function () {
		return function(err, val) {
			if (err) {
				this.throw(err);
			} else {
				this.return(val);
			}
		}.bind(this);
	}
```
- example usage
```shell
...
*/
Future.prototype.isResolved = function() { ... }

/**
* Returns a node-style function which will mark this future as resolved when called.
*
* Example usage:
*   var errback = aFuture.resolver();
*   asyncFunction(arg1, arg2, etc, errback)
*   var result = aFuture.wait();
*/
Future.prototype.resolver = function() { ... }

/**
* Waits for this future to resolve and then invokes a callback.
...
```

#### <a name="apidoc.element.fibers.future.prototype.return"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>return (value)](#apidoc.element.fibers.future.prototype.return)
- description and source-code
```javascript
return = function (value) {
		if (this.resolved) {
			throw new Error('Future resolved more than once');
		}
		this.value = value;
		this.resolved = true;

		var callbacks = this.callbacks;
		if (callbacks) {
			delete this.callbacks;
			for (var ii = 0; ii < callbacks.length; ++ii) {
				try {
					var ref = callbacks[ii];
					if (ref[1]) {
						ref[1](value);
					} else {
						ref[0](undefined, value);
					}
				} catch(ex) {
					// console.log('Resolve cb threw', String(ex.stack || ex.message || ex));
					process.nextTick(function() {
						throw(ex);
					});
				}
			}
		}
	}
```
- example usage
```shell
...
var Future = require('fibers/future'), wait = Future.wait;

// This function returns a future which resolves after a timeout. This
// demonstrates manually resolving futures.
function sleep(ms) {
	var future = new Future;
	setTimeout(function() {
		future.return();
	}, ms);
	return future;
}

// You can create functions which automatically run in their own fiber and
// return futures that resolve when the fiber returns (this probably sounds
// confusing.. just play with it to understand).
...
```

#### <a name="apidoc.element.fibers.future.prototype.throw"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>throw (error)](#apidoc.element.fibers.future.prototype.throw)
- description and source-code
```javascript
throw = function (error) {
		if (this.resolved) {
			throw new Error('Future resolved more than once');
		} else if (!error) {
			throw new Error('Must throw non-empty error');
		}
		this.error = error;
		this.resolved = true;

		var callbacks = this.callbacks;
		if (callbacks) {
			delete this.callbacks;
			for (var ii = 0; ii < callbacks.length; ++ii) {
				try {
					var ref = callbacks[ii];
					if (ref[1]) {
						ref[0].throw(error);
					} else {
						ref[0](error);
					}
				} catch(ex) {
					// console.log('Resolve cb threw', String(ex.stack || ex.message || ex));
					process.nextTick(function() {
						throw(ex);
					});
				}
			}
		}
	}
```
- example usage
```shell
...
/**
* Throw from this future as returned. All pending callbacks will be invoked immediately.
* Note that execution will continue normally after running this method,
* so make sure you exit appropriately after running throw()
*
* error - the error to throw when get() or wait() is called.
*
* Example usage: aFuture.throw(new Error("Something borked"))
*/
Future.prototype.throw = function(error) { ... }

/**
* "detach" this future. Basically this is useful if you want to run a task in a future, you
* aren't interested in its return value, but if it throws you don't want the exception to be
* lost. If this fiber throws, an exception will be thrown to the event loop and node will
...
```

#### <a name="apidoc.element.fibers.future.prototype.wait"></a>[function <span class="apidocSignatureSpan">fibers.future.prototype.</span>wait ()](#apidoc.element.fibers.future.prototype.wait)
- description and source-code
```javascript
wait = function () {
		if (this.isResolved()) {
			return this.get();
		}
		Future.wait(this);
		return this.get();
	}
```
- example usage
```shell
...

'''javascript
var Future = require('fibers/future');
var fs = Future.wrap(require('fs'));

Future.task(function() {
	// Get a list of files in the directory
	var fileNames = fs.readdirFuture('.').wait();
	console.log('Found '+ fileNames.length+ ' files');

	// Stat each file
	var stats = [];
	for (var ii = 0; ii < fileNames.length; ++ii) {
		stats.push(fs.statFuture(fileNames[ii]));
	}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
