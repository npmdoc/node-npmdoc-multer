# api documentation for  [multer (v1.3.0)](https://github.com/expressjs/multer#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-multer.svg)](https://travis-ci.org/npmdoc/node-npmdoc-multer)
#### Middleware for handling `multipart/form-data`.

[![NPM](https://nodei.co/npm/multer.png?downloads=true)](https://www.npmjs.com/package/multer)

[![apidoc](https://npmdoc.github.io/node-npmdoc-multer/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-multer_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-multer/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-multer/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/expressjs/multer/issues"
    },
    "contributors": [
        {
            "name": "Hage Yaapa",
            "email": "captain@hacksparrow.com",
            "url": "http://www.hacksparrow.com"
        },
        {
            "name": "Jaret Pfluger",
            "email": "https://github.com/jpfluger"
        },
        {
            "name": "Linus Unnebäck",
            "email": "linus@folkdatorn.se"
        }
    ],
    "dependencies": {
        "append-field": "^0.1.0",
        "busboy": "^0.2.11",
        "concat-stream": "^1.5.0",
        "mkdirp": "^0.5.1",
        "object-assign": "^3.0.0",
        "on-finished": "^2.3.0",
        "type-is": "^1.6.4",
        "xtend": "^4.0.0"
    },
    "description": "Middleware for handling 'multipart/form-data'.",
    "devDependencies": {
        "express": "^4.13.1",
        "form-data": "^1.0.0-rc1",
        "fs-temp": "^0.1.2",
        "mocha": "^2.2.5",
        "rimraf": "^2.4.1",
        "standard": "^8.2.0",
        "testdata-w3c-json-form": "^0.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "092b2670f6846fa4914965efc8cf94c20fec6cd2",
        "tarball": "https://registry.npmjs.org/multer/-/multer-1.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "files": [
        "LICENSE",
        "index.js",
        "storage/",
        "lib/"
    ],
    "gitHead": "7ef2e81215e9b773204df44fb4aee29e58340061",
    "homepage": "https://github.com/expressjs/multer#readme",
    "keywords": [
        "form",
        "post",
        "multipart",
        "form-data",
        "formdata",
        "express",
        "middleware"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "hacksparrow",
            "email": "captain@hacksparrow.com"
        },
        {
            "name": "linusu",
            "email": "linus@folkdatorn.se"
        },
        {
            "name": "jpfluger",
            "email": "japes@aberlorn.com"
        }
    ],
    "name": "multer",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/expressjs/multer.git"
    },
    "scripts": {
        "test": "standard && mocha"
    },
    "version": "1.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module multer](#apidoc.module.multer)
1.  [function <span class="apidocSignatureSpan">multer.</span>counter ()](#apidoc.element.multer.counter)
1.  [function <span class="apidocSignatureSpan">multer.</span>diskStorage (opts)](#apidoc.element.multer.diskStorage)
1.  [function <span class="apidocSignatureSpan">multer.</span>file_appender (strategy, req)](#apidoc.element.multer.file_appender)
1.  [function <span class="apidocSignatureSpan">multer.</span>memoryStorage (opts)](#apidoc.element.multer.memoryStorage)
1.  object <span class="apidocSignatureSpan">multer.</span>counter.prototype
1.  object <span class="apidocSignatureSpan">multer.</span>file_appender.prototype

#### [module multer.counter](#apidoc.module.multer.counter)
1.  [function <span class="apidocSignatureSpan">multer.</span>counter ()](#apidoc.element.multer.counter.counter)

#### [module multer.counter.prototype](#apidoc.module.multer.counter.prototype)
1.  [function <span class="apidocSignatureSpan">multer.counter.prototype.</span>decrement ()](#apidoc.element.multer.counter.prototype.decrement)
1.  [function <span class="apidocSignatureSpan">multer.counter.prototype.</span>increment ()](#apidoc.element.multer.counter.prototype.increment)
1.  [function <span class="apidocSignatureSpan">multer.counter.prototype.</span>isZero ()](#apidoc.element.multer.counter.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">multer.counter.prototype.</span>onceZero (fn)](#apidoc.element.multer.counter.prototype.onceZero)

#### [module multer.file_appender](#apidoc.module.multer.file_appender)
1.  [function <span class="apidocSignatureSpan">multer.</span>file_appender (strategy, req)](#apidoc.element.multer.file_appender.file_appender)

#### [module multer.file_appender.prototype](#apidoc.module.multer.file_appender.prototype)
1.  [function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>insertPlaceholder (file)](#apidoc.element.multer.file_appender.prototype.insertPlaceholder)
1.  [function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>removePlaceholder (placeholder)](#apidoc.element.multer.file_appender.prototype.removePlaceholder)
1.  [function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>replacePlaceholder (placeholder, file)](#apidoc.element.multer.file_appender.prototype.replacePlaceholder)



# <a name="apidoc.module.multer"></a>[module multer](#apidoc.module.multer)

#### <a name="apidoc.element.multer.counter"></a>[function <span class="apidocSignatureSpan">multer.</span>counter ()](#apidoc.element.multer.counter)
- description and source-code
```javascript
function Counter() {
  EventEmitter.call(this)
  this.value = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.multer.diskStorage"></a>[function <span class="apidocSignatureSpan">multer.</span>diskStorage (opts)](#apidoc.element.multer.diskStorage)
- description and source-code
```javascript
diskStorage = function (opts) {
  return new DiskStorage(opts)
}
```
- example usage
```shell
...
### 'storage'

#### 'DiskStorage'

The disk storage engine gives you full control on storing files to disk.

'''javascript
var storage = multer.diskStorage({
  destination: function (req, file, cb) {
    cb(null, '/tmp/my-uploads')
  },
  filename: function (req, file, cb) {
    cb(null, file.fieldname + '-' + Date.now())
  }
})
...
```

#### <a name="apidoc.element.multer.file_appender"></a>[function <span class="apidocSignatureSpan">multer.</span>file_appender (strategy, req)](#apidoc.element.multer.file_appender)
- description and source-code
```javascript
function FileAppender(strategy, req) {
  this.strategy = strategy
  this.req = req

  switch (strategy) {
    case 'NONE': break
    case 'VALUE': break
    case 'ARRAY': req.files = []; break
    case 'OBJECT': req.files = Object.create(null); break
    default: throw new Error('Unknown file strategy: ' + strategy)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.multer.memoryStorage"></a>[function <span class="apidocSignatureSpan">multer.</span>memoryStorage (opts)](#apidoc.element.multer.memoryStorage)
- description and source-code
```javascript
memoryStorage = function (opts) {
  return new MemoryStorage(opts)
}
```
- example usage
```shell
...

#### 'MemoryStorage'

The memory storage engine stores the files in memory as 'Buffer' objects. It
doesn't have any options.

'''javascript
var storage = multer.memoryStorage()
var upload = multer({ storage: storage })
'''

When using memory storage, the file info will contain a field called
'buffer' that contains the entire file.

**WARNING**: Uploading very large files, or relatively small files in large
...
```



# <a name="apidoc.module.multer.counter"></a>[module multer.counter](#apidoc.module.multer.counter)

#### <a name="apidoc.element.multer.counter.counter"></a>[function <span class="apidocSignatureSpan">multer.</span>counter ()](#apidoc.element.multer.counter.counter)
- description and source-code
```javascript
function Counter() {
  EventEmitter.call(this)
  this.value = 0
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.multer.counter.prototype"></a>[module multer.counter.prototype](#apidoc.module.multer.counter.prototype)

#### <a name="apidoc.element.multer.counter.prototype.decrement"></a>[function <span class="apidocSignatureSpan">multer.counter.prototype.</span>decrement ()](#apidoc.element.multer.counter.prototype.decrement)
- description and source-code
```javascript
function decrement() {
  if (--this.value === 0) this.emit('zero')
}
```
- example usage
```shell
...
Object.defineProperty(file, 'stream', {
  configurable: true,
  enumerable: false,
  value: fileStream
})

fileStream.on('error', function (err) {
  pendingWrites.decrement()
  abortWithError(err)
})

fileStream.on('limit', function () {
  aborting = true
  abortWithCode('LIMIT_FILE_SIZE', fieldname)
})
...
```

#### <a name="apidoc.element.multer.counter.prototype.increment"></a>[function <span class="apidocSignatureSpan">multer.counter.prototype.</span>increment ()](#apidoc.element.multer.counter.prototype.increment)
- description and source-code
```javascript
function increment() {
  this.value++
}
```
- example usage
```shell
...

if (!includeFile) {
  appender.removePlaceholder(placeholder)
  return fileStream.resume()
}

var aborting = false
pendingWrites.increment()

Object.defineProperty(file, 'stream', {
  configurable: true,
  enumerable: false,
  value: fileStream
})
...
```

#### <a name="apidoc.element.multer.counter.prototype.isZero"></a>[function <span class="apidocSignatureSpan">multer.counter.prototype.</span>isZero ()](#apidoc.element.multer.counter.prototype.isZero)
- description and source-code
```javascript
function isZero() {
  return (this.value === 0)
}
```
- example usage
```shell
...
}

Counter.prototype.isZero = function isZero () {
  return (this.value === 0)
}

Counter.prototype.onceZero = function onceZero (fn) {
  if (this.isZero()) return fn()

  this.once('zero', fn)
}

module.exports = Counter
...
```

#### <a name="apidoc.element.multer.counter.prototype.onceZero"></a>[function <span class="apidocSignatureSpan">multer.counter.prototype.</span>onceZero (fn)](#apidoc.element.multer.counter.prototype.onceZero)
- description and source-code
```javascript
function onceZero(fn) {
  if (this.isZero()) return fn()

  this.once('zero', fn)
}
```
- example usage
```shell
...
      if (readFinished && pendingWrites.isZero() && !errorOccured) done()
    }

    function abortWithError (uploadError) {
      if (errorOccured) return
      errorOccured = true

      pendingWrites.onceZero(function () {
function remove (file, cb) {
  storage._removeFile(req, file, cb)
}

removeUploadedFiles(uploadedFiles, remove, function (err, storageErrors) {
  if (err) return done(err)
...
```



# <a name="apidoc.module.multer.file_appender"></a>[module multer.file_appender](#apidoc.module.multer.file_appender)

#### <a name="apidoc.element.multer.file_appender.file_appender"></a>[function <span class="apidocSignatureSpan">multer.</span>file_appender (strategy, req)](#apidoc.element.multer.file_appender.file_appender)
- description and source-code
```javascript
function FileAppender(strategy, req) {
  this.strategy = strategy
  this.req = req

  switch (strategy) {
    case 'NONE': break
    case 'VALUE': break
    case 'ARRAY': req.files = []; break
    case 'OBJECT': req.files = Object.create(null); break
    default: throw new Error('Unknown file strategy: ' + strategy)
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.multer.file_appender.prototype"></a>[module multer.file_appender.prototype](#apidoc.module.multer.file_appender.prototype)

#### <a name="apidoc.element.multer.file_appender.prototype.insertPlaceholder"></a>[function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>insertPlaceholder (file)](#apidoc.element.multer.file_appender.prototype.insertPlaceholder)
- description and source-code
```javascript
insertPlaceholder = function (file) {
  var placeholder = {
    fieldname: file.fieldname
  }

  switch (this.strategy) {
    case 'NONE': break
    case 'VALUE': break
    case 'ARRAY': this.req.files.push(placeholder); break
    case 'OBJECT':
      if (this.req.files[file.fieldname]) {
        this.req.files[file.fieldname].push(placeholder)
      } else {
        this.req.files[file.fieldname] = [placeholder]
      }
      break
  }

  return placeholder
}
```
- example usage
```shell
...
var file = {
  fieldname: fieldname,
  originalname: filename,
  encoding: encoding,
  mimetype: mimetype
}

var placeholder = appender.insertPlaceholder(file)

fileFilter(req, file, function (err, includeFile) {
  if (err) {
    appender.removePlaceholder(placeholder)
    return abortWithError(err)
  }
...
```

#### <a name="apidoc.element.multer.file_appender.prototype.removePlaceholder"></a>[function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>removePlaceholder (placeholder)](#apidoc.element.multer.file_appender.prototype.removePlaceholder)
- description and source-code
```javascript
removePlaceholder = function (placeholder) {
  switch (this.strategy) {
    case 'NONE': break
    case 'VALUE': break
    case 'ARRAY': arrayRemove(this.req.files, placeholder); break
    case 'OBJECT':
      if (this.req.files[placeholder.fieldname].length === 1) {
        delete this.req.files[placeholder.fieldname]
      } else {
        arrayRemove(this.req.files[placeholder.fieldname], placeholder)
      }
      break
  }
}
```
- example usage
```shell
...
mimetype: mimetype
      }

      var placeholder = appender.insertPlaceholder(file)

      fileFilter(req, file, function (err, includeFile) {
if (err) {
  appender.removePlaceholder(placeholder)
  return abortWithError(err)
}

if (!includeFile) {
  appender.removePlaceholder(placeholder)
  return fileStream.resume()
}
...
```

#### <a name="apidoc.element.multer.file_appender.prototype.replacePlaceholder"></a>[function <span class="apidocSignatureSpan">multer.file_appender.prototype.</span>replacePlaceholder (placeholder, file)](#apidoc.element.multer.file_appender.prototype.replacePlaceholder)
- description and source-code
```javascript
replacePlaceholder = function (placeholder, file) {
  if (this.strategy === 'VALUE') {
    this.req.file = file
    return
  }

  delete placeholder.fieldname
  objectAssign(placeholder, file)
}
```
- example usage
```shell
...
        appender.removePlaceholder(placeholder)
        pendingWrites.decrement()
        return abortWithError(err)
      }

      var fileInfo = extend(file, info)

      appender.replacePlaceholder(placeholder, fileInfo)
      uploadedFiles.push(fileInfo)
      pendingWrites.decrement()
      indicateDone()
    })
  })
})
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
