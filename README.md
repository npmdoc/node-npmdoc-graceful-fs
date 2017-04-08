# api documentation for  [graceful-fs (v4.1.11)](https://github.com/isaacs/node-graceful-fs#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-graceful-fs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-graceful-fs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-graceful-fs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-graceful-fs)
#### A drop-in replacement for fs, making various improvements.

[![NPM](https://nodei.co/npm/graceful-fs.png?downloads=true)](https://www.npmjs.com/package/graceful-fs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-graceful-fs/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-graceful-fs%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-graceful-fs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-graceful-fs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-graceful-fs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/isaacs/node-graceful-fs/issues"
    },
    "dependencies": {},
    "description": "A drop-in replacement for fs, making various improvements.",
    "devDependencies": {
        "mkdirp": "^0.5.0",
        "rimraf": "^2.2.8",
        "tap": "^5.4.2"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "0e8bdfe4d1ddb8854d64e04ea7c00e2a026e5658",
        "tarball": "https://registry.npmjs.org/graceful-fs/-/graceful-fs-4.1.11.tgz"
    },
    "engines": {
        "node": ">=0.4.0"
    },
    "files": [
        "fs.js",
        "graceful-fs.js",
        "legacy-streams.js",
        "polyfills.js"
    ],
    "gitHead": "65cf80d1fd3413b823c16c626c1e7c326452bee5",
    "homepage": "https://github.com/isaacs/node-graceful-fs#readme",
    "keywords": [
        "fs",
        "module",
        "reading",
        "retry",
        "retries",
        "queue",
        "error",
        "errors",
        "handling",
        "EMFILE",
        "EAGAIN",
        "EINVAL",
        "EPERM",
        "EACCESS"
    ],
    "license": "ISC",
    "main": "graceful-fs.js",
    "maintainers": [
        {
            "name": "isaacs",
            "email": "i@izs.me"
        }
    ],
    "name": "graceful-fs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/isaacs/node-graceful-fs.git"
    },
    "scripts": {
        "test": "node test.js | tap -"
    },
    "version": "4.1.11"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module graceful-fs](#apidoc.module.graceful-fs)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>FileReadStream (path, options)](#apidoc.element.graceful-fs.FileReadStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>FileWriteStream (path, options)](#apidoc.element.graceful-fs.FileWriteStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>ReadStream (path, options)](#apidoc.element.graceful-fs.ReadStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.graceful-fs.Stats)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>WriteStream (path, options)](#apidoc.element.graceful-fs.WriteStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>_toUnixTimestamp (time)](#apidoc.element.graceful-fs._toUnixTimestamp)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>access (path, mode, callback)](#apidoc.element.graceful-fs.access)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>accessSync (path, mode)](#apidoc.element.graceful-fs.accessSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>appendFile (path, data, options, cb)](#apidoc.element.graceful-fs.appendFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>appendFileSync (path, data, options)](#apidoc.element.graceful-fs.appendFileSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>chmod (target, mode, cb)](#apidoc.element.graceful-fs.chmod)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>chmodSync (target, mode)](#apidoc.element.graceful-fs.chmodSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>chown (target, uid, gid, cb)](#apidoc.element.graceful-fs.chown)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>chownSync (target, uid, gid)](#apidoc.element.graceful-fs.chownSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>close (fd, cb)](#apidoc.element.graceful-fs.close)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>closeSync (fd)](#apidoc.element.graceful-fs.closeSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>createReadStream (path, options)](#apidoc.element.graceful-fs.createReadStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>createWriteStream (path, options)](#apidoc.element.graceful-fs.createWriteStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>exists (path, callback)](#apidoc.element.graceful-fs.exists)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>existsSync (path)](#apidoc.element.graceful-fs.existsSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fchmod (target, mode, cb)](#apidoc.element.graceful-fs.fchmod)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fchmodSync (target, mode)](#apidoc.element.graceful-fs.fchmodSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fchown (target, uid, gid, cb)](#apidoc.element.graceful-fs.fchown)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fchownSync (target, uid, gid)](#apidoc.element.graceful-fs.fchownSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fdatasync (fd, callback)](#apidoc.element.graceful-fs.fdatasync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fdatasyncSync (fd)](#apidoc.element.graceful-fs.fdatasyncSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fstat (target, cb)](#apidoc.element.graceful-fs.fstat)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fstatSync (target)](#apidoc.element.graceful-fs.fstatSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fsync (fd, callback)](#apidoc.element.graceful-fs.fsync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>fsyncSync (fd)](#apidoc.element.graceful-fs.fsyncSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>ftruncate (fd, len, callback)](#apidoc.element.graceful-fs.ftruncate)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>ftruncateSync (fd, len)](#apidoc.element.graceful-fs.ftruncateSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.graceful-fs.futimes)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>futimesSync (fd, atime, mtime)](#apidoc.element.graceful-fs.futimesSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>gracefulify (fs)](#apidoc.element.graceful-fs.gracefulify)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lchmod (path, mode, cb)](#apidoc.element.graceful-fs.lchmod)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lchmodSync ()](#apidoc.element.graceful-fs.lchmodSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lchown (path, uid, gid, cb)](#apidoc.element.graceful-fs.lchown)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lchownSync ()](#apidoc.element.graceful-fs.lchownSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>link (existingPath, newPath, callback)](#apidoc.element.graceful-fs.link)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>linkSync (existingPath, newPath)](#apidoc.element.graceful-fs.linkSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lstat (target, cb)](#apidoc.element.graceful-fs.lstat)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lstatSync (target)](#apidoc.element.graceful-fs.lstatSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lutimes (_a, _b, _c, cb)](#apidoc.element.graceful-fs.lutimes)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>lutimesSync ()](#apidoc.element.graceful-fs.lutimesSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>mkdir (path, mode, callback)](#apidoc.element.graceful-fs.mkdir)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>mkdirSync (path, mode)](#apidoc.element.graceful-fs.mkdirSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>mkdtemp (prefix, options, callback)](#apidoc.element.graceful-fs.mkdtemp)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>mkdtempSync (prefix, options)](#apidoc.element.graceful-fs.mkdtempSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>open (path, flags, mode, cb)](#apidoc.element.graceful-fs.open)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>openSync (path, flags, mode)](#apidoc.element.graceful-fs.openSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>read (fd, buffer, offset, length, position, callback_)](#apidoc.element.graceful-fs.read)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readFile (path, options, cb)](#apidoc.element.graceful-fs.readFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readFileSync (path, options)](#apidoc.element.graceful-fs.readFileSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readSync (fd, buffer, offset, length, position)](#apidoc.element.graceful-fs.readSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readdir (path, options, cb)](#apidoc.element.graceful-fs.readdir)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readdirSync (path, options)](#apidoc.element.graceful-fs.readdirSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readlink (path, options, callback)](#apidoc.element.graceful-fs.readlink)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>readlinkSync (path, options)](#apidoc.element.graceful-fs.readlinkSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>realpath (p, options, callback)](#apidoc.element.graceful-fs.realpath)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>realpathSync (p, options)](#apidoc.element.graceful-fs.realpathSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>rename (oldPath, newPath, callback)](#apidoc.element.graceful-fs.rename)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>renameSync (oldPath, newPath)](#apidoc.element.graceful-fs.renameSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>rmdir (path, callback)](#apidoc.element.graceful-fs.rmdir)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>rmdirSync (path)](#apidoc.element.graceful-fs.rmdirSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>stat (target, cb)](#apidoc.element.graceful-fs.stat)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>statSync (target)](#apidoc.element.graceful-fs.statSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>symlink (target, path, type_, callback_)](#apidoc.element.graceful-fs.symlink)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>symlinkSync (target, path, type)](#apidoc.element.graceful-fs.symlinkSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>truncate (path, len, callback)](#apidoc.element.graceful-fs.truncate)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>truncateSync (path, len)](#apidoc.element.graceful-fs.truncateSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>unlink (path, callback)](#apidoc.element.graceful-fs.unlink)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>unlinkSync (path)](#apidoc.element.graceful-fs.unlinkSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>unwatchFile (filename, listener)](#apidoc.element.graceful-fs.unwatchFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>utimes (path, atime, mtime, callback)](#apidoc.element.graceful-fs.utimes)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>utimesSync (path, atime, mtime)](#apidoc.element.graceful-fs.utimesSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>watch (filename, options, listener)](#apidoc.element.graceful-fs.watch)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>watchFile (filename, options, listener)](#apidoc.element.graceful-fs.watchFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.graceful-fs.write)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>writeFile (path, data, options, cb)](#apidoc.element.graceful-fs.writeFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>writeFileSync (path, data, options)](#apidoc.element.graceful-fs.writeFileSync)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>writeSync (fd, buffer, offset, length, position)](#apidoc.element.graceful-fs.writeSync)
1.  number <span class="apidocSignatureSpan">graceful-fs.</span>F_OK
1.  number <span class="apidocSignatureSpan">graceful-fs.</span>R_OK
1.  number <span class="apidocSignatureSpan">graceful-fs.</span>W_OK
1.  number <span class="apidocSignatureSpan">graceful-fs.</span>X_OK
1.  object <span class="apidocSignatureSpan">graceful-fs.</span>ReadStream.prototype
1.  object <span class="apidocSignatureSpan">graceful-fs.</span>Stats.prototype
1.  object <span class="apidocSignatureSpan">graceful-fs.</span>WriteStream.prototype
1.  object <span class="apidocSignatureSpan">graceful-fs.</span>constants

#### [module graceful-fs.ReadStream](#apidoc.module.graceful-fs.ReadStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>ReadStream (path, options)](#apidoc.element.graceful-fs.ReadStream.ReadStream)

#### [module graceful-fs.ReadStream.prototype](#apidoc.module.graceful-fs.ReadStream.prototype)
1.  [function <span class="apidocSignatureSpan">graceful-fs.ReadStream.prototype.</span>open ()](#apidoc.element.graceful-fs.ReadStream.prototype.open)

#### [module graceful-fs.Stats](#apidoc.module.graceful-fs.Stats)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.graceful-fs.Stats.Stats)

#### [module graceful-fs.Stats.prototype](#apidoc.module.graceful-fs.Stats.prototype)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>_checkModeProperty (property)](#apidoc.element.graceful-fs.Stats.prototype._checkModeProperty)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isBlockDevice ()](#apidoc.element.graceful-fs.Stats.prototype.isBlockDevice)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isCharacterDevice ()](#apidoc.element.graceful-fs.Stats.prototype.isCharacterDevice)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isDirectory ()](#apidoc.element.graceful-fs.Stats.prototype.isDirectory)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isFIFO ()](#apidoc.element.graceful-fs.Stats.prototype.isFIFO)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isFile ()](#apidoc.element.graceful-fs.Stats.prototype.isFile)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isSocket ()](#apidoc.element.graceful-fs.Stats.prototype.isSocket)
1.  [function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isSymbolicLink ()](#apidoc.element.graceful-fs.Stats.prototype.isSymbolicLink)

#### [module graceful-fs.WriteStream](#apidoc.module.graceful-fs.WriteStream)
1.  [function <span class="apidocSignatureSpan">graceful-fs.</span>WriteStream (path, options)](#apidoc.element.graceful-fs.WriteStream.WriteStream)

#### [module graceful-fs.WriteStream.prototype](#apidoc.module.graceful-fs.WriteStream.prototype)
1.  [function <span class="apidocSignatureSpan">graceful-fs.WriteStream.prototype.</span>open ()](#apidoc.element.graceful-fs.WriteStream.prototype.open)



# <a name="apidoc.module.graceful-fs"></a>[module graceful-fs](#apidoc.module.graceful-fs)

#### <a name="apidoc.element.graceful-fs.FileReadStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>FileReadStream (path, options)](#apidoc.element.graceful-fs.FileReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.FileWriteStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>FileWriteStream (path, options)](#apidoc.element.graceful-fs.FileWriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.ReadStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>ReadStream (path, options)](#apidoc.element.graceful-fs.ReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.graceful-fs.Stats)
- description and source-code
```javascript
function Stats( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec) {
  this.dev = dev;
  this.mode = mode;
  this.nlink = nlink;
  this.uid = uid;
  this.gid = gid;
  this.rdev = rdev;
  this.blksize = blksize;
  this.ino = ino;
  this.size = size;
  this.blocks = blocks;
  this.atime = new Date(atim_msec);
  this.mtime = new Date(mtim_msec);
  this.ctime = new Date(ctim_msec);
  this.birthtime = new Date(birthtim_msec);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.WriteStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>WriteStream (path, options)](#apidoc.element.graceful-fs.WriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs._toUnixTimestamp"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>_toUnixTimestamp (time)](#apidoc.element.graceful-fs._toUnixTimestamp)
- description and source-code
```javascript
function toUnixTimestamp(time) {
  if (typeof time === 'string' && +time == time) {
    return +time;
  }
  if (typeof time === 'number') {
    if (!Number.isFinite(time) || time < 0) {
      return Date.now() / 1000;
    }
    return time;
  }
  if (util.isDate(time)) {
    // convert to 123.456 UNIX timestamp
    return time.getTime() / 1000;
  }
  throw new Error('Cannot parse time: ' + time);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.access"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>access (path, mode, callback)](#apidoc.element.graceful-fs.access)
- description and source-code
```javascript
access = function (path, mode, callback) {
  if (typeof mode === 'function') {
    callback = mode;
    mode = fs.F_OK;
  } else if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  if (!nullCheck(path, callback))
    return;

  mode = mode | 0;
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.access(pathModule._makeLong(path), mode, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.accessSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>accessSync (path, mode)](#apidoc.element.graceful-fs.accessSync)
- description and source-code
```javascript
accessSync = function (path, mode) {
  nullCheck(path);

  if (mode === undefined)
    mode = fs.F_OK;
  else
    mode = mode | 0;

  binding.access(pathModule._makeLong(path), mode);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.appendFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>appendFile (path, data, options, cb)](#apidoc.element.graceful-fs.appendFile)
- description and source-code
```javascript
function appendFile(path, data, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$appendFile(path, data, options, cb)

  function go$appendFile (path, data, options, cb) {
    return fs$appendFile(path, data, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$appendFile, [path, data, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.appendFileSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>appendFileSync (path, data, options)](#apidoc.element.graceful-fs.appendFileSync)
- description and source-code
```javascript
appendFileSync = function (path, data, options) {
  if (!options) {
    options = { encoding: 'utf8', mode: 0o666, flag: 'a' };
  } else if (typeof options === 'string') {
    options = { encoding: options, mode: 0o666, flag: 'a' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  if (!options.flag)
    options = util._extend({ flag: 'a' }, options);

  // force append behavior when using a supplied file descriptor
  if (isFd(path))
    options.flag = 'a';

  fs.writeFileSync(path, data, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.chmod"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>chmod (target, mode, cb)](#apidoc.element.graceful-fs.chmod)
- description and source-code
```javascript
chmod = function (target, mode, cb) {
  return orig.call(fs, target, mode, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.chmodSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>chmodSync (target, mode)](#apidoc.element.graceful-fs.chmodSync)
- description and source-code
```javascript
chmodSync = function (target, mode) {
  try {
    return orig.call(fs, target, mode)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.chown"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>chown (target, uid, gid, cb)](#apidoc.element.graceful-fs.chown)
- description and source-code
```javascript
chown = function (target, uid, gid, cb) {
  return orig.call(fs, target, uid, gid, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.chownSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>chownSync (target, uid, gid)](#apidoc.element.graceful-fs.chownSync)
- description and source-code
```javascript
chownSync = function (target, uid, gid) {
  try {
    return orig.call(fs, target, uid, gid)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.close"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>close (fd, cb)](#apidoc.element.graceful-fs.close)
- description and source-code
```javascript
close = function (fd, cb) {
  return fs$close.call(fs, fd, function (err) {
    if (!err)
      retry()

    if (typeof cb === 'function')
      cb.apply(this, arguments)
  })
}
```
- example usage
```shell
...
    if (err) {
      if (callback) callback(err)
      return
    }
    // prefer to return the chmod error, if one occurs,
    // but still try to close, and report closing errors if they occur.
    fs.fchmod(fd, mode, function (err) {
      fs.close(fd, function(err2) {
        if (callback) callback(err || err2)
      })
    })
  })
}

fs.lchmodSync = function (path, mode) {
...
```

#### <a name="apidoc.element.graceful-fs.closeSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>closeSync (fd)](#apidoc.element.graceful-fs.closeSync)
- description and source-code
```javascript
closeSync = function (fd) {
  // Note that graceful-fs also retries when fs.closeSync() fails.
  // Looks like a bug to me, although it's probably a harmless one.
  var rval = fs$closeSync.apply(fs, arguments)
  retry()
  return rval
}
```
- example usage
```shell
...
    if (typeof cb === 'function')
      cb.apply(this, arguments)
  })
}})(fs.close)

module.exports.closeSync =
fs.closeSync = (function (fs$closeSync) { return function (fd) {
  // Note that graceful-fs also retries when fs.closeSync() fails.
  // Looks like a bug to me, although it's probably a harmless one.
  var rval = fs$closeSync.apply(fs, arguments)
  retry()
  return rval
}})(fs.closeSync)

function patch (fs) {
...
```

#### <a name="apidoc.element.graceful-fs.createReadStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>createReadStream (path, options)](#apidoc.element.graceful-fs.createReadStream)
- description and source-code
```javascript
function createReadStream(path, options) {
  return new ReadStream(path, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.createWriteStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>createWriteStream (path, options)](#apidoc.element.graceful-fs.createWriteStream)
- description and source-code
```javascript
function createWriteStream(path, options) {
  return new WriteStream(path, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.exists"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>exists (path, callback)](#apidoc.element.graceful-fs.exists)
- description and source-code
```javascript
exists = function (path, callback) {
  if (!nullCheck(path, cb)) return;
  var req = new FSReqWrap();
  req.oncomplete = cb;
  binding.stat(pathModule._makeLong(path), req);
  function cb(err, stats) {
    if (callback) callback(err ? false : true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.existsSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>existsSync (path)](#apidoc.element.graceful-fs.existsSync)
- description and source-code
```javascript
existsSync = function (path) {
  try {
    nullCheck(path);
    binding.stat(pathModule._makeLong(path), statValues);
    return true;
  } catch (e) {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fchmod"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fchmod (target, mode, cb)](#apidoc.element.graceful-fs.fchmod)
- description and source-code
```javascript
fchmod = function (target, mode, cb) {
  return orig.call(fs, target, mode, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
...
         , function (err, fd) {
    if (err) {
      if (callback) callback(err)
      return
    }
    // prefer to return the chmod error, if one occurs,
    // but still try to close, and report closing errors if they occur.
    fs.fchmod(fd, mode, function (err) {
      fs.close(fd, function(err2) {
        if (callback) callback(err || err2)
      })
    })
  })
}
...
```

#### <a name="apidoc.element.graceful-fs.fchmodSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fchmodSync (target, mode)](#apidoc.element.graceful-fs.fchmodSync)
- description and source-code
```javascript
fchmodSync = function (target, mode) {
  try {
    return orig.call(fs, target, mode)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
...
var fd = fs.openSync(path, constants.O_WRONLY | constants.O_SYMLINK, mode)

// prefer to return the chmod error, if one occurs,
// but still try to close, and report closing errors if they occur.
var threw = true
var ret
try {
  ret = fs.fchmodSync(fd, mode)
  threw = false
} finally {
  if (threw) {
    try {
      fs.closeSync(fd)
    } catch (er) {}
  } else {
...
```

#### <a name="apidoc.element.graceful-fs.fchown"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fchown (target, uid, gid, cb)](#apidoc.element.graceful-fs.fchown)
- description and source-code
```javascript
fchown = function (target, uid, gid, cb) {
  return orig.call(fs, target, uid, gid, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fchownSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fchownSync (target, uid, gid)](#apidoc.element.graceful-fs.fchownSync)
- description and source-code
```javascript
fchownSync = function (target, uid, gid) {
  try {
    return orig.call(fs, target, uid, gid)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fdatasync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fdatasync (fd, callback)](#apidoc.element.graceful-fs.fdatasync)
- description and source-code
```javascript
fdatasync = function (fd, callback) {
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.fdatasync(fd, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fdatasyncSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fdatasyncSync (fd)](#apidoc.element.graceful-fs.fdatasyncSync)
- description and source-code
```javascript
fdatasyncSync = function (fd) {
  return binding.fdatasync(fd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fstat"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fstat (target, cb)](#apidoc.element.graceful-fs.fstat)
- description and source-code
```javascript
fstat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fstatSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fstatSync (target)](#apidoc.element.graceful-fs.fstatSync)
- description and source-code
```javascript
fstatSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fsync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fsync (fd, callback)](#apidoc.element.graceful-fs.fsync)
- description and source-code
```javascript
fsync = function (fd, callback) {
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.fsync(fd, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.fsyncSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>fsyncSync (fd)](#apidoc.element.graceful-fs.fsyncSync)
- description and source-code
```javascript
fsyncSync = function (fd) {
  return binding.fsync(fd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.ftruncate"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>ftruncate (fd, len, callback)](#apidoc.element.graceful-fs.ftruncate)
- description and source-code
```javascript
ftruncate = function (fd, len, callback) {
  if (typeof len === 'function') {
    callback = len;
    len = 0;
  } else if (len === undefined) {
    len = 0;
  }
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.ftruncate(fd, len, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.ftruncateSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>ftruncateSync (fd, len)](#apidoc.element.graceful-fs.ftruncateSync)
- description and source-code
```javascript
ftruncateSync = function (fd, len) {
  if (len === undefined) {
    len = 0;
  }
  return binding.ftruncate(fd, len);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.futimes"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.graceful-fs.futimes)
- description and source-code
```javascript
futimes = function (fd, atime, mtime, callback) {
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.futimes(fd, atime, mtime, req);
}
```
- example usage
```shell
...
  if (constants.hasOwnProperty("O_SYMLINK")) {
fs.lutimes = function (path, at, mt, cb) {
  fs.open(path, constants.O_SYMLINK, function (er, fd) {
    if (er) {
      if (cb) cb(er)
      return
    }
    fs.futimes(fd, at, mt, function (er) {
      fs.close(fd, function (er2) {
        if (cb) cb(er || er2)
      })
    })
  })
}
...
```

#### <a name="apidoc.element.graceful-fs.futimesSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>futimesSync (fd, atime, mtime)](#apidoc.element.graceful-fs.futimesSync)
- description and source-code
```javascript
futimesSync = function (fd, atime, mtime) {
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  binding.futimes(fd, atime, mtime);
}
```
- example usage
```shell
...
}

fs.lutimesSync = function (path, at, mt) {
  var fd = fs.openSync(path, constants.O_SYMLINK)
  var ret
  var threw = true
  try {
    ret = fs.futimesSync(fd, at, mt)
    threw = false
  } finally {
    if (threw) {
      try {
        fs.closeSync(fd)
      } catch (er) {}
    } else {
...
```

#### <a name="apidoc.element.graceful-fs.gracefulify"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>gracefulify (fs)](#apidoc.element.graceful-fs.gracefulify)
- description and source-code
```javascript
function patch(fs) {
  // Everything that references the open() function needs to be in here
  polyfills(fs)
  fs.gracefulify = patch
  fs.FileReadStream = ReadStream;  // Legacy name.
  fs.FileWriteStream = WriteStream;  // Legacy name.
  fs.createReadStream = createReadStream
  fs.createWriteStream = createWriteStream
  var fs$readFile = fs.readFile
  fs.readFile = readFile
  function readFile (path, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$readFile(path, options, cb)

    function go$readFile (path, options, cb) {
      return fs$readFile(path, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$readFile, [path, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$writeFile = fs.writeFile
  fs.writeFile = writeFile
  function writeFile (path, data, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$writeFile(path, data, options, cb)

    function go$writeFile (path, data, options, cb) {
      return fs$writeFile(path, data, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$writeFile, [path, data, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$appendFile = fs.appendFile
  if (fs$appendFile)
    fs.appendFile = appendFile
  function appendFile (path, data, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$appendFile(path, data, options, cb)

    function go$appendFile (path, data, options, cb) {
      return fs$appendFile(path, data, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$appendFile, [path, data, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$readdir = fs.readdir
  fs.readdir = readdir
  function readdir (path, options, cb) {
    var args = [path]
    if (typeof options !== 'function') {
      args.push(options)
    } else {
      cb = options
    }
    args.push(go$readdir$cb)

    return go$readdir(args)

    function go$readdir$cb (err, files) {
      if (files && files.sort)
        files.sort()

      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$readdir, [args]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    }
  }

  function go$readdir (args) {
    return fs$readdir.apply(fs, args)
  }

  if (process.version.substr(0, 4) === 'v0.8') {
    var legStreams = legacy(fs)
    ReadStream = legStreams.ReadStream
    WriteStream = legStreams.WriteStream
  }

  var fs$ReadStream = fs.ReadStream
  ReadStream.prototype = Object.create(fs$ReadStream.prototype)
  ReadStream.prototype.open = ReadStream$open

  var fs$WriteStream = fs.WriteStream
  WriteStream.prototype = Object.create(fs$WriteStream.prototype)
  WriteStream.prototype.open = WriteStream$open

  fs.ReadStream = ReadStream
  fs.WriteStream = WriteStream

  function ReadStream (path, options) {
    if (this instanceof ReadStream)
      return fs$ReadStream.apply(this, arguments), this
    else
      return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
  }

  function ReadStream$open () {
    var that = this
    open(that.path, that.flags, that.mode, function (err, fd) {
      if (err) {
        if (that.autoClose)
          that.destroy()

        that.emit('error', err)
      } else {
        that.fd = fd
        that.emit('open', fd)
        that.read()
      }
    })
  }

  function WriteStream (path, options) {
    if (this instanceof WriteStream)
      return fs$WriteStream.apply(this, arguments), this
    else
      return W ...
```
- example usage
```shell
...
If you want to patch the global fs module (or any other fs-like
module) you can do this:

'''javascript
// Make sure to read the caveat below.
var realFs = require('fs')
var gracefulFs = require('graceful-fs')
gracefulFs.gracefulify(realFs)
'''

This should only ever be done at the top-level application layer, in
order to delay on EMFILE errors from any fs-using dependencies.  You
should **not** do this in a library, because it can cause unexpected
delays in other parts of the program.
...
```

#### <a name="apidoc.element.graceful-fs.lchmod"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lchmod (path, mode, cb)](#apidoc.element.graceful-fs.lchmod)
- description and source-code
```javascript
lchmod = function (path, mode, cb) {
  if (cb) process.nextTick(cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lchmodSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lchmodSync ()](#apidoc.element.graceful-fs.lchmodSync)
- description and source-code
```javascript
lchmodSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lchown"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lchown (path, uid, gid, cb)](#apidoc.element.graceful-fs.lchown)
- description and source-code
```javascript
lchown = function (path, uid, gid, cb) {
  if (cb) process.nextTick(cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lchownSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lchownSync ()](#apidoc.element.graceful-fs.lchownSync)
- description and source-code
```javascript
lchownSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.link"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>link (existingPath, newPath, callback)](#apidoc.element.graceful-fs.link)
- description and source-code
```javascript
link = function (existingPath, newPath, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(existingPath, callback)) return;
  if (!nullCheck(newPath, callback)) return;

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.link(pathModule._makeLong(existingPath),
               pathModule._makeLong(newPath),
               req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.linkSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>linkSync (existingPath, newPath)](#apidoc.element.graceful-fs.linkSync)
- description and source-code
```javascript
linkSync = function (existingPath, newPath) {
  nullCheck(existingPath);
  nullCheck(newPath);
  return binding.link(pathModule._makeLong(existingPath),
                      pathModule._makeLong(newPath));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lstat"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lstat (target, cb)](#apidoc.element.graceful-fs.lstat)
- description and source-code
```javascript
lstat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lstatSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lstatSync (target)](#apidoc.element.graceful-fs.lstatSync)
- description and source-code
```javascript
lstatSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lutimes"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lutimes (_a, _b, _c, cb)](#apidoc.element.graceful-fs.lutimes)
- description and source-code
```javascript
lutimes = function (_a, _b, _c, cb) { if (cb) process.nextTick(cb) }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.lutimesSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>lutimesSync ()](#apidoc.element.graceful-fs.lutimesSync)
- description and source-code
```javascript
lutimesSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.mkdir"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>mkdir (path, mode, callback)](#apidoc.element.graceful-fs.mkdir)
- description and source-code
```javascript
mkdir = function (path, mode, callback) {
  if (typeof mode === 'function') callback = mode;
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.mkdir(pathModule._makeLong(path),
                modeNum(mode, 0o777),
                req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.mkdirSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>mkdirSync (path, mode)](#apidoc.element.graceful-fs.mkdirSync)
- description and source-code
```javascript
mkdirSync = function (path, mode) {
  nullCheck(path);
  return binding.mkdir(pathModule._makeLong(path),
                       modeNum(mode, 0o777));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.mkdtemp"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>mkdtemp (prefix, options, callback)](#apidoc.element.graceful-fs.mkdtemp)
- description and source-code
```javascript
mkdtemp = function (prefix, options, callback) {
  if (!prefix || typeof prefix !== 'string')
    throw new TypeError('filename prefix is required');

  options = options || {};
  if (typeof options === 'function') {
    callback = options;
    options = {};
  } else if (typeof options === 'string') {
    options = {encoding: options};
  }
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');

  callback = makeCallback(callback);
  if (!nullCheck(prefix, callback)) {
    return;
  }

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.mkdtemp(prefix + 'XXXXXX', options.encoding, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.mkdtempSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>mkdtempSync (prefix, options)](#apidoc.element.graceful-fs.mkdtempSync)
- description and source-code
```javascript
mkdtempSync = function (prefix, options) {
  if (!prefix || typeof prefix !== 'string')
    throw new TypeError('filename prefix is required');

  options = options || {};
  if (typeof options === 'string')
    options = {encoding: options};
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');
  nullCheck(prefix);

  return binding.mkdtemp(prefix + 'XXXXXX', options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.open"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>open (path, flags, mode, cb)](#apidoc.element.graceful-fs.open)
- description and source-code
```javascript
function open(path, flags, mode, cb) {
  if (typeof mode === 'function')
    cb = mode, mode = null

  return go$open(path, flags, mode, cb)

  function go$open (path, flags, mode, cb) {
    return fs$open(path, flags, mode, function (err, fd) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$open, [path, flags, mode, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
...
    if (this.fd !== null) {
process.nextTick(function() {
  self._read();
});
return;
    }

    fs.open(this.path, this.flags, this.mode, function (err, fd) {
if (err) {
  self.emit('error', err);
  self.readable = false;
  return;
}

self.fd = fd;
...
```

#### <a name="apidoc.element.graceful-fs.openSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>openSync (path, flags, mode)](#apidoc.element.graceful-fs.openSync)
- description and source-code
```javascript
openSync = function (path, flags, mode) {
  mode = modeNum(mode, 0o666);
  nullCheck(path);
  return binding.open(pathModule._makeLong(path), stringToFlags(flags), mode);
}
```
- example usage
```shell
...
      if (callback) callback(err || err2)
    })
  })
})
  }

  fs.lchmodSync = function (path, mode) {
var fd = fs.openSync(path, constants.O_WRONLY | constants.O_SYMLINK, mode)

// prefer to return the chmod error, if one occurs,
// but still try to close, and report closing errors if they occur.
var threw = true
var ret
try {
  ret = fs.fchmodSync(fd, mode)
...
```

#### <a name="apidoc.element.graceful-fs.read"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>read (fd, buffer, offset, length, position, callback_)](#apidoc.element.graceful-fs.read)
- description and source-code
```javascript
read = function (fd, buffer, offset, length, position, callback_) {
  var callback
  if (callback_ && typeof callback_ === 'function') {
    var eagCounter = 0
    callback = function (er, _, __) {
      if (er && er.code === 'EAGAIN' && eagCounter < 10) {
        eagCounter ++
        return fs$read.call(fs, fd, buffer, offset, length, position, callback)
      }
      callback_.apply(this, arguments)
    }
  }
  return fs$read.call(fs, fd, buffer, offset, length, position, callback)
}
```
- example usage
```shell
...
      if (that.autoClose)
        that.destroy()

      that.emit('error', err)
    } else {
      that.fd = fd
      that.emit('open', fd)
      that.read()
    }
  })
}

function WriteStream (path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
...
```

#### <a name="apidoc.element.graceful-fs.readFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readFile (path, options, cb)](#apidoc.element.graceful-fs.readFile)
- description and source-code
```javascript
function readFile(path, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$readFile(path, options, cb)

  function go$readFile (path, options, cb) {
    return fs$readFile(path, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$readFile, [path, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.readFileSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readFileSync (path, options)](#apidoc.element.graceful-fs.readFileSync)
- description and source-code
```javascript
readFileSync = function (path, options) {
  if (!options) {
    options = { encoding: null, flag: 'r' };
  } else if (typeof options === 'string') {
    options = { encoding: options, flag: 'r' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  var encoding = options.encoding;
  assertEncoding(encoding);

  var flag = options.flag || 'r';
  var isUserFd = isFd(path); // file descriptor ownership
  var fd = isUserFd ? path : fs.openSync(path, flag, 0o666);

  var st = tryStatSync(fd, isUserFd);
  var size = st.isFile() ? st.size : 0;
  var pos = 0;
  var buffer; // single buffer with file data
  var buffers; // list for when size is unknown

  if (size === 0) {
    buffers = [];
  } else {
    buffer = tryCreateBuffer(size, fd, isUserFd);
  }

  var bytesRead;

  if (size !== 0) {
    do {
      bytesRead = tryReadSync(fd, isUserFd, buffer, pos, size - pos);
      pos += bytesRead;
    } while (bytesRead !== 0 && pos < size);
  } else {
    do {
      // the kernel lies about many files.
      // Go ahead and try to read some bytes.
      buffer = Buffer.allocUnsafe(8192);
      bytesRead = tryReadSync(fd, isUserFd, buffer, 0, 8192);
      if (bytesRead !== 0) {
        buffers.push(buffer.slice(0, bytesRead));
      }
      pos += bytesRead;
    } while (bytesRead !== 0);
  }

  if (!isUserFd)
    fs.closeSync(fd);

  if (size === 0) {
    // data was collected into the buffers list.
    buffer = Buffer.concat(buffers, pos);
  } else if (pos < size) {
    buffer = buffer.slice(0, pos);
  }

  if (encoding) buffer = buffer.toString(encoding);
  return buffer;
}
```
- example usage
```shell
...
## USAGE

'''javascript
// use just like fs
var fs = require('graceful-fs')

// now go and do stuff with it...
fs.readFileSync('some-file-or-whatever')
'''

## Global Patching

If you want to patch the global fs module (or any other fs-like
module) you can do this:
...
```

#### <a name="apidoc.element.graceful-fs.readSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readSync (fd, buffer, offset, length, position)](#apidoc.element.graceful-fs.readSync)
- description and source-code
```javascript
readSync = function (fd, buffer, offset, length, position) {
  var eagCounter = 0
  while (true) {
    try {
      return fs$readSync.call(fs, fd, buffer, offset, length, position)
    } catch (er) {
      if (er.code === 'EAGAIN' && eagCounter < 10) {
        eagCounter ++
        continue
      }
      throw er
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.readdir"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readdir (path, options, cb)](#apidoc.element.graceful-fs.readdir)
- description and source-code
```javascript
function readdir(path, options, cb) {
  var args = [path]
  if (typeof options !== 'function') {
    args.push(options)
  } else {
    cb = options
  }
  args.push(go$readdir$cb)

  return go$readdir(args)

  function go$readdir$cb (err, files) {
    if (files && files.sort)
      files.sort()

    if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
      enqueue([go$readdir, [args]])
    else {
      if (typeof cb === 'function')
        cb.apply(this, arguments)
      retry()
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.readdirSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readdirSync (path, options)](#apidoc.element.graceful-fs.readdirSync)
- description and source-code
```javascript
readdirSync = function (path, options) {
  options = options || {};
  if (typeof options === 'string')
    options = {encoding: options};
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');
  nullCheck(path);
  return binding.readdir(pathModule._makeLong(path), options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.readlink"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readlink (path, options, callback)](#apidoc.element.graceful-fs.readlink)
- description and source-code
```javascript
readlink = function (path, options, callback) {
  options = options || {};
  if (typeof options === 'function') {
    callback = options;
    options = {};
  } else if (typeof options === 'string') {
    options = {encoding: options};
  }
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.readlink(pathModule._makeLong(path), options.encoding, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.readlinkSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>readlinkSync (path, options)](#apidoc.element.graceful-fs.readlinkSync)
- description and source-code
```javascript
readlinkSync = function (path, options) {
  options = options || {};
  if (typeof options === 'string')
    options = {encoding: options};
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');
  nullCheck(path);
  return binding.readlink(pathModule._makeLong(path), options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.realpath"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>realpath (p, options, callback)](#apidoc.element.graceful-fs.realpath)
- description and source-code
```javascript
function realpath(p, options, callback) {
  if (typeof callback !== 'function') {
    callback = maybeCallback(options);
    options = {};
  }

  if (!options) {
    options = {};
  } else if (typeof options === 'function') {
    options = {};
  } else if (typeof options === 'string') {
    options = {encoding: options};
  } else if (typeof options !== 'object') {
    throw new TypeError('"options" must be a string or an object');
  }
  if (!nullCheck(p, callback))
    return;

  p = p.toString('utf8');
  p = pathModule.resolve(p);

  const seenLinks = {};
  const knownHard = {};

  // current character position in p
  var pos;
  // the partial path so far, including a trailing slash if any
  var current;
  // the partial path without a trailing slash (except when pointing at a root)
  var base;
  // the partial path scanned in the previous round, with slash
  var previous;

  start();

  function start() {
    // Skip over roots
    var m = splitRootRe.exec(p);
    pos = m[0].length;
    current = m[0];
    base = m[0];
    previous = '';

    // On windows, check that the root exists. On unix there is no need.
    if (isWindows && !knownHard[base]) {
      fs.lstat(base, function(err) {
        if (err) return callback(err);
        knownHard[base] = true;
        LOOP();
      });
    } else {
      process.nextTick(LOOP);
    }
  }

  // walk down the path, swapping out linked pathparts for their real
  // values
  function LOOP() {
    // stop if scanned past end of path
    if (pos >= p.length) {
      return callback(null, encodeRealpathResult(p, options));
    }

    // find the next part
    nextPartRe.lastIndex = pos;
    var result = nextPartRe.exec(p);
    previous = current;
    current += result[0];
    base = previous + result[1];
    pos = nextPartRe.lastIndex;

    // continue if not a symlink
    if (knownHard[base]) {
      return process.nextTick(LOOP);
    }

    return fs.lstat(base, gotStat);
  }

  function gotStat(err, stat) {
    if (err) return callback(err);

    // if not a symlink, skip to the next path part
    if (!stat.isSymbolicLink()) {
      knownHard[base] = true;
      return process.nextTick(LOOP);
    }

    // stat & read the link if not read before
    // call gotTarget as soon as the link target is known
    // dev/ino always return 0 on windows, so skip the check.
    let id;
    if (!isWindows) {
      id = '${stat.dev.toString(32)}:${stat.ino.toString(32)}';
      if (seenLinks.hasOwnProperty(id)) {
        return gotTarget(null, seenLinks[id], base);
      }
    }
    fs.stat(base, function(err) {
      if (err) return callback(err);

      fs.readlink(base, function(err, target) {
        if (!isWindows) seenLinks[id] = target;
        gotTarget(err, target);
      });
    });
  }

  function gotTarget(err, target, base) {
    if (err) return callback(err);

    var resolvedLink = pathModule.resolve(previous, target);
    gotResolvedLink(resolvedLink);
  }

  function gotResolvedLink(resolvedLink) {
    // resolve the link, then start over
    p = pathModule.resolve(resolvedLink, p.slice(pos));
    start();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.realpathSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>realpathSync (p, options)](#apidoc.element.graceful-fs.realpathSync)
- description and source-code
```javascript
function realpathSync(p, options) {
  if (!options)
    options = {};
  else if (typeof options === 'string')
    options = {encoding: options};
  else if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');
  nullCheck(p);

  p = p.toString('utf8');
  p = pathModule.resolve(p);

  const seenLinks = {};
  const knownHard = {};
  const cache = options[realpathCacheKey];
  const original = p;

  const maybeCachedResult = cache && cache.get(p);
  if (maybeCachedResult) {
    return maybeCachedResult;
  }

  // current character position in p
  var pos;
  // the partial path so far, including a trailing slash if any
  var current;
  // the partial path without a trailing slash (except when pointing at a root)
  var base;
  // the partial path scanned in the previous round, with slash
  var previous;

  start();

  function start() {
    // Skip over roots
    var m = splitRootRe.exec(p);
    pos = m[0].length;
    current = m[0];
    base = m[0];
    previous = '';

    // On windows, check that the root exists. On unix there is no need.
    if (isWindows && !knownHard[base]) {
      fs.lstatSync(base);
      knownHard[base] = true;
    }
  }

  // walk down the path, swapping out linked pathparts for their real
  // values
  // NB: p.length changes.
  while (pos < p.length) {
    // find the next part
    nextPartRe.lastIndex = pos;
    var result = nextPartRe.exec(p);
    previous = current;
    current += result[0];
    base = previous + result[1];
    pos = nextPartRe.lastIndex;

    // continue if not a symlink
    if (knownHard[base] || (cache && cache.get(base) === base)) {
      continue;
    }

    var resolvedLink;
    const maybeCachedResolved = cache && cache.get(base);
    if (maybeCachedResolved) {
      resolvedLink = maybeCachedResolved;
    } else {
      var stat = fs.lstatSync(base);
      if (!stat.isSymbolicLink()) {
        knownHard[base] = true;
        if (cache) cache.set(base, base);
        continue;
      }

      // read the link if it wasn't read before
      // dev/ino always return 0 on windows, so skip the check.
      let linkTarget = null;
      let id;
      if (!isWindows) {
        id = '${stat.dev.toString(32)}:${stat.ino.toString(32)}';
        if (seenLinks.hasOwnProperty(id)) {
          linkTarget = seenLinks[id];
        }
      }
      if (linkTarget === null) {
        fs.statSync(base);
        linkTarget = fs.readlinkSync(base);
      }
      resolvedLink = pathModule.resolve(previous, linkTarget);

      if (cache) cache.set(base, resolvedLink);
      if (!isWindows) seenLinks[id] = linkTarget;
    }

    // resolve the link, then start over
    p = pathModule.resolve(resolvedLink, p.slice(pos));
    start();
  }

  if (cache) cache.set(original, p);
  return encodeRealpathResult(p, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.rename"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>rename (oldPath, newPath, callback)](#apidoc.element.graceful-fs.rename)
- description and source-code
```javascript
rename = function (oldPath, newPath, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(oldPath, callback)) return;
  if (!nullCheck(newPath, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rename(pathModule._makeLong(oldPath),
                 pathModule._makeLong(newPath),
                 req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.renameSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>renameSync (oldPath, newPath)](#apidoc.element.graceful-fs.renameSync)
- description and source-code
```javascript
renameSync = function (oldPath, newPath) {
  nullCheck(oldPath);
  nullCheck(newPath);
  return binding.rename(pathModule._makeLong(oldPath),
                        pathModule._makeLong(newPath));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.rmdir"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>rmdir (path, callback)](#apidoc.element.graceful-fs.rmdir)
- description and source-code
```javascript
rmdir = function (path, callback) {
  callback = maybeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rmdir(pathModule._makeLong(path), req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.rmdirSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>rmdirSync (path)](#apidoc.element.graceful-fs.rmdirSync)
- description and source-code
```javascript
rmdirSync = function (path) {
  nullCheck(path);
  return binding.rmdir(pathModule._makeLong(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.stat"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>stat (target, cb)](#apidoc.element.graceful-fs.stat)
- description and source-code
```javascript
stat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
...
var start = Date.now()
var backoff = 0;
fs$rename(from, to, function CB (er) {
  if (er
      && (er.code === "EACCES" || er.code === "EPERM")
      && Date.now() - start < 60000) {
    setTimeout(function() {
      fs.stat(to, function (stater, st) {
        if (stater && stater.code === "ENOENT")
          fs$rename(from, to, CB);
        else
          cb(er)
      })
    }, backoff)
    if (backoff < 100)
...
```

#### <a name="apidoc.element.graceful-fs.statSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>statSync (target)](#apidoc.element.graceful-fs.statSync)
- description and source-code
```javascript
statSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.symlink"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>symlink (target, path, type_, callback_)](#apidoc.element.graceful-fs.symlink)
- description and source-code
```javascript
symlink = function (target, path, type_, callback_) {
  var type = (typeof type_ === 'string' ? type_ : null);
  var callback = makeCallback(arguments[arguments.length - 1]);

  if (!nullCheck(target, callback)) return;
  if (!nullCheck(path, callback)) return;

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.symlink(preprocessSymlinkDestination(target, type, path),
                  pathModule._makeLong(path),
                  type,
                  req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.symlinkSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>symlinkSync (target, path, type)](#apidoc.element.graceful-fs.symlinkSync)
- description and source-code
```javascript
symlinkSync = function (target, path, type) {
  type = (typeof type === 'string' ? type : null);

  nullCheck(target);
  nullCheck(path);

  return binding.symlink(preprocessSymlinkDestination(target, type, path),
                         pathModule._makeLong(path),
                         type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.truncate"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>truncate (path, len, callback)](#apidoc.element.graceful-fs.truncate)
- description and source-code
```javascript
truncate = function (path, len, callback) {
  if (typeof path === 'number') {
    return fs.ftruncate(path, len, callback);
  }
  if (typeof len === 'function') {
    callback = len;
    len = 0;
  } else if (len === undefined) {
    len = 0;
  }

  callback = maybeCallback(callback);
  fs.open(path, 'r+', function(er, fd) {
    if (er) return callback(er);
    var req = new FSReqWrap();
    req.oncomplete = function oncomplete(er) {
      fs.close(fd, function(er2) {
        callback(er || er2);
      });
    };
    binding.ftruncate(fd, len, req);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.truncateSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>truncateSync (path, len)](#apidoc.element.graceful-fs.truncateSync)
- description and source-code
```javascript
truncateSync = function (path, len) {
  if (typeof path === 'number') {
    // legacy
    return fs.ftruncateSync(path, len);
  }
  if (len === undefined) {
    len = 0;
  }
  // allow error to be thrown, but still close fd.
  var fd = fs.openSync(path, 'r+');
  var ret;

  try {
    ret = fs.ftruncateSync(fd, len);
  } finally {
    fs.closeSync(fd);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.unlink"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>unlink (path, callback)](#apidoc.element.graceful-fs.unlink)
- description and source-code
```javascript
unlink = function (path, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.unlink(pathModule._makeLong(path), req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.unlinkSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>unlinkSync (path)](#apidoc.element.graceful-fs.unlinkSync)
- description and source-code
```javascript
unlinkSync = function (path) {
  nullCheck(path);
  return binding.unlink(pathModule._makeLong(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.unwatchFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>unwatchFile (filename, listener)](#apidoc.element.graceful-fs.unwatchFile)
- description and source-code
```javascript
unwatchFile = function (filename, listener) {
  nullCheck(filename);
  filename = pathModule.resolve(filename);
  var stat = statWatchers.get(filename);

  if (stat === undefined) return;

  if (typeof listener === 'function') {
    stat.removeListener('change', listener);
  } else {
    stat.removeAllListeners('change');
  }

  if (stat.listenerCount('change') === 0) {
    stat.stop();
    statWatchers.delete(filename);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.utimes"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>utimes (path, atime, mtime, callback)](#apidoc.element.graceful-fs.utimes)
- description and source-code
```javascript
utimes = function (path, atime, mtime, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.utimes(pathModule._makeLong(path),
                 toUnixTimestamp(atime),
                 toUnixTimestamp(mtime),
                 req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.utimesSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>utimesSync (path, atime, mtime)](#apidoc.element.graceful-fs.utimesSync)
- description and source-code
```javascript
utimesSync = function (path, atime, mtime) {
  nullCheck(path);
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  binding.utimes(pathModule._makeLong(path), atime, mtime);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.watch"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>watch (filename, options, listener)](#apidoc.element.graceful-fs.watch)
- description and source-code
```javascript
watch = function (filename, options, listener) {
  nullCheck(filename);

  options = options || {};
  if (typeof options === 'function') {
    listener = options;
    options = {};
  } else if (typeof options === 'string') {
    options = {encoding: options};
  }
  if (typeof options !== 'object')
    throw new TypeError('"options" must be a string or an object');

  if (options.persistent === undefined) options.persistent = true;
  if (options.recursive === undefined) options.recursive = false;

  const watcher = new FSWatcher();
  watcher.start(filename,
                options.persistent,
                options.recursive,
                options.encoding);

  if (listener) {
    watcher.addListener('change', listener);
  }

  return watcher;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.watchFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>watchFile (filename, options, listener)](#apidoc.element.graceful-fs.watchFile)
- description and source-code
```javascript
watchFile = function (filename, options, listener) {
  nullCheck(filename);
  filename = pathModule.resolve(filename);
  var stat;

  var defaults = {
    // Poll interval in milliseconds. 5007 is what libev used to use. It's
    // a little on the slow side but let's stick with it for now to keep
    // behavioral changes to a minimum.
    interval: 5007,
    persistent: true
  };

  if (options !== null && typeof options === 'object') {
    options = util._extend(defaults, options);
  } else {
    listener = options;
    options = defaults;
  }

  if (typeof listener !== 'function') {
    throw new Error('"watchFile()" requires a listener function');
  }

  stat = statWatchers.get(filename);

  if (stat === undefined) {
    stat = new StatWatcher();
    stat.start(filename, options.persistent, options.interval);
    statWatchers.set(filename, stat);
  }

  stat.addListener('change', listener);
  return stat;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.write"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.graceful-fs.write)
- description and source-code
```javascript
write = function (fd, buffer, offset, length, position, callback) {
  function wrapper(err, written) {
    // Retain a reference to buffer so that it can't be GC'ed too soon.
    callback(err, written || 0, buffer);
  }

  var req = new FSReqWrap();
  req.oncomplete = wrapper;

  if (buffer instanceof Buffer) {
    // if no position is passed then assume null
    if (typeof position === 'function') {
      callback = position;
      position = null;
    }
    callback = maybeCallback(callback);
    return binding.writeBuffer(fd, buffer, offset, length, position, req);
  }

  if (typeof buffer !== 'string')
    buffer += '';
  if (typeof position !== 'function') {
    if (typeof offset === 'function') {
      position = offset;
      offset = null;
    } else {
      position = length;
    }
    length = 'utf8';
  }
  callback = maybeCallback(position);
  return binding.writeString(fd, buffer, offset, length, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.writeFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>writeFile (path, data, options, cb)](#apidoc.element.graceful-fs.writeFile)
- description and source-code
```javascript
function writeFile(path, data, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$writeFile(path, data, options, cb)

  function go$writeFile (path, data, options, cb) {
    return fs$writeFile(path, data, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$writeFile, [path, data, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.writeFileSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>writeFileSync (path, data, options)](#apidoc.element.graceful-fs.writeFileSync)
- description and source-code
```javascript
writeFileSync = function (path, data, options) {
  if (!options) {
    options = { encoding: 'utf8', mode: 0o666, flag: 'w' };
  } else if (typeof options === 'string') {
    options = { encoding: options, mode: 0o666, flag: 'w' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  assertEncoding(options.encoding);

  var flag = options.flag || 'w';
  var isUserFd = isFd(path); // file descriptor ownership
  var fd = isUserFd ? path : fs.openSync(path, flag, options.mode);

  if (!(data instanceof Buffer)) {
    data = Buffer.from('' + data, options.encoding || 'utf8');
  }
  var offset = 0;
  var length = data.length;
  var position = /a/.test(flag) ? null : 0;
  try {
    while (length > 0) {
      var written = fs.writeSync(fd, data, offset, length, position);
      offset += written;
      length -= written;
      if (position !== null) {
        position += written;
      }
    }
  } finally {
    if (!isUserFd) fs.closeSync(fd);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.writeSync"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>writeSync (fd, buffer, offset, length, position)](#apidoc.element.graceful-fs.writeSync)
- description and source-code
```javascript
writeSync = function (fd, buffer, offset, length, position) {
  if (buffer instanceof Buffer) {
    if (position === undefined)
      position = null;
    return binding.writeBuffer(fd, buffer, offset, length, position);
  }
  if (typeof buffer !== 'string')
    buffer += '';
  if (offset === undefined)
    offset = null;
  return binding.writeString(fd, buffer, offset, length, position);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graceful-fs.ReadStream"></a>[module graceful-fs.ReadStream](#apidoc.module.graceful-fs.ReadStream)

#### <a name="apidoc.element.graceful-fs.ReadStream.ReadStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>ReadStream (path, options)](#apidoc.element.graceful-fs.ReadStream.ReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graceful-fs.ReadStream.prototype"></a>[module graceful-fs.ReadStream.prototype](#apidoc.module.graceful-fs.ReadStream.prototype)

#### <a name="apidoc.element.graceful-fs.ReadStream.prototype.open"></a>[function <span class="apidocSignatureSpan">graceful-fs.ReadStream.prototype.</span>open ()](#apidoc.element.graceful-fs.ReadStream.prototype.open)
- description and source-code
```javascript
function ReadStream$open() {
  var that = this
  open(that.path, that.flags, that.mode, function (err, fd) {
    if (err) {
      if (that.autoClose)
        that.destroy()

      that.emit('error', err)
    } else {
      that.fd = fd
      that.emit('open', fd)
      that.read()
    }
  })
}
```
- example usage
```shell
...
    if (this.fd !== null) {
process.nextTick(function() {
  self._read();
});
return;
    }

    fs.open(this.path, this.flags, this.mode, function (err, fd) {
if (err) {
  self.emit('error', err);
  self.readable = false;
  return;
}

self.fd = fd;
...
```



# <a name="apidoc.module.graceful-fs.Stats"></a>[module graceful-fs.Stats](#apidoc.module.graceful-fs.Stats)

#### <a name="apidoc.element.graceful-fs.Stats.Stats"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.graceful-fs.Stats.Stats)
- description and source-code
```javascript
function Stats( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec) {
  this.dev = dev;
  this.mode = mode;
  this.nlink = nlink;
  this.uid = uid;
  this.gid = gid;
  this.rdev = rdev;
  this.blksize = blksize;
  this.ino = ino;
  this.size = size;
  this.blocks = blocks;
  this.atime = new Date(atim_msec);
  this.mtime = new Date(mtim_msec);
  this.ctime = new Date(ctim_msec);
  this.birthtime = new Date(birthtim_msec);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graceful-fs.Stats.prototype"></a>[module graceful-fs.Stats.prototype](#apidoc.module.graceful-fs.Stats.prototype)

#### <a name="apidoc.element.graceful-fs.Stats.prototype._checkModeProperty"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>_checkModeProperty (property)](#apidoc.element.graceful-fs.Stats.prototype._checkModeProperty)
- description and source-code
```javascript
_checkModeProperty = function (property) {
  return ((this.mode & constants.S_IFMT) === property);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isBlockDevice"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isBlockDevice ()](#apidoc.element.graceful-fs.Stats.prototype.isBlockDevice)
- description and source-code
```javascript
isBlockDevice = function () {
  return this._checkModeProperty(constants.S_IFBLK);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isCharacterDevice"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isCharacterDevice ()](#apidoc.element.graceful-fs.Stats.prototype.isCharacterDevice)
- description and source-code
```javascript
isCharacterDevice = function () {
  return this._checkModeProperty(constants.S_IFCHR);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isDirectory"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isDirectory ()](#apidoc.element.graceful-fs.Stats.prototype.isDirectory)
- description and source-code
```javascript
isDirectory = function () {
  return this._checkModeProperty(constants.S_IFDIR);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isFIFO"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isFIFO ()](#apidoc.element.graceful-fs.Stats.prototype.isFIFO)
- description and source-code
```javascript
isFIFO = function () {
  return this._checkModeProperty(constants.S_IFIFO);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isFile"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isFile ()](#apidoc.element.graceful-fs.Stats.prototype.isFile)
- description and source-code
```javascript
isFile = function () {
  return this._checkModeProperty(constants.S_IFREG);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isSocket"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isSocket ()](#apidoc.element.graceful-fs.Stats.prototype.isSocket)
- description and source-code
```javascript
isSocket = function () {
  return this._checkModeProperty(constants.S_IFSOCK);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graceful-fs.Stats.prototype.isSymbolicLink"></a>[function <span class="apidocSignatureSpan">graceful-fs.Stats.prototype.</span>isSymbolicLink ()](#apidoc.element.graceful-fs.Stats.prototype.isSymbolicLink)
- description and source-code
```javascript
isSymbolicLink = function () {
  return this._checkModeProperty(constants.S_IFLNK);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graceful-fs.WriteStream"></a>[module graceful-fs.WriteStream](#apidoc.module.graceful-fs.WriteStream)

#### <a name="apidoc.element.graceful-fs.WriteStream.WriteStream"></a>[function <span class="apidocSignatureSpan">graceful-fs.</span>WriteStream (path, options)](#apidoc.element.graceful-fs.WriteStream.WriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graceful-fs.WriteStream.prototype"></a>[module graceful-fs.WriteStream.prototype](#apidoc.module.graceful-fs.WriteStream.prototype)

#### <a name="apidoc.element.graceful-fs.WriteStream.prototype.open"></a>[function <span class="apidocSignatureSpan">graceful-fs.WriteStream.prototype.</span>open ()](#apidoc.element.graceful-fs.WriteStream.prototype.open)
- description and source-code
```javascript
function WriteStream$open() {
  var that = this
  open(that.path, that.flags, that.mode, function (err, fd) {
    if (err) {
      that.destroy()
      that.emit('error', err)
    } else {
      that.fd = fd
      that.emit('open', fd)
    }
  })
}
```
- example usage
```shell
...
    if (this.fd !== null) {
process.nextTick(function() {
  self._read();
});
return;
    }

    fs.open(this.path, this.flags, this.mode, function (err, fd) {
if (err) {
  self.emit('error', err);
  self.readable = false;
  return;
}

self.fd = fd;
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
