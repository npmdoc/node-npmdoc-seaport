# api documentation for  [seaport (v2.0.9)](https://github.com/substack/seaport)  [![npm package](https://img.shields.io/npm/v/npmdoc-seaport.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-seaport) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-seaport.svg)](https://travis-ci.org/npmdoc/node-npmdoc-seaport)
#### service registry and port assignment for clusters

[![NPM](https://nodei.co/npm/seaport.png?downloads=true)](https://www.npmjs.com/package/seaport)

[![apidoc](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-seaport_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-seaport/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "James Halliday",
        "email": "mail@substack.net",
        "url": "http://substack.net"
    },
    "bin": {
        "seaport": "bin/cmd.js"
    },
    "browser": "lib/seaport.js",
    "bugs": {
        "url": "https://github.com/substack/seaport/issues"
    },
    "dependencies": {
        "defined": "~0.0.0",
        "indexof": "~0.0.1",
        "inherits": "~1.0.0",
        "merge": "~1.1.2",
        "object-keys": "~0.5.0",
        "optimist": "~0.3.5",
        "readable-stream": "~1.0.26",
        "secure-peer": "~0.2.1",
        "semver": "~1.1.0",
        "split": "~0.3.0",
        "stream-combiner": "~0.0.4",
        "through": "~2.3.4"
    },
    "description": "service registry and port assignment for clusters",
    "devDependencies": {
        "async": "~0.9.0",
        "destroyer": "~0.0.0",
        "macgyver": "~1.10.1",
        "tap": "~0.4.9"
    },
    "directories": {
        "example": "example",
        "test": "test"
    },
    "dist": {
        "shasum": "576da25a9aaac77b9841757d966866ffdde46076",
        "tarball": "https://registry.npmjs.org/seaport/-/seaport-2.0.9.tgz"
    },
    "engine": {
        "node": ">=0.8"
    },
    "gitHead": "ad9c46ed3162bb14f4766c6f0f0fc1dfc3b9b3bc",
    "homepage": "https://github.com/substack/seaport",
    "keywords": [
        "port",
        "allocate",
        "hub",
        "service",
        "registry",
        "roles"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "substack",
            "email": "mail@substack.net"
        }
    ],
    "name": "seaport",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/substack/seaport.git"
    },
    "scripts": {
        "test": "tap test/*.js"
    },
    "version": "2.0.9"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module seaport](#apidoc.module.seaport)
1.  [function <span class="apidocSignatureSpan"></span>seaport (opts)](#apidoc.element.seaport.seaport)
1.  [function <span class="apidocSignatureSpan">seaport.</span>connect ()](#apidoc.element.seaport.connect)
1.  [function <span class="apidocSignatureSpan">seaport.</span>createServer (opts)](#apidoc.element.seaport.createServer)
1.  [function <span class="apidocSignatureSpan">seaport.</span>protocol (opts)](#apidoc.element.seaport.protocol)
1.  [function <span class="apidocSignatureSpan">seaport.</span>super ()](#apidoc.element.seaport.super)
1.  object <span class="apidocSignatureSpan">seaport.</span>protocol.prototype
1.  object <span class="apidocSignatureSpan">seaport.</span>seaport.prototype

#### [module seaport.protocol](#apidoc.module.seaport.protocol)
1.  [function <span class="apidocSignatureSpan">seaport.</span>protocol (opts)](#apidoc.element.seaport.protocol.protocol)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.</span>super (options)](#apidoc.element.seaport.protocol.super)

#### [module seaport.protocol.prototype](#apidoc.module.seaport.protocol.prototype)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>_read (size)](#apidoc.element.seaport.protocol.prototype._read)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>_write (row, enc, next)](#apidoc.element.seaport.protocol.prototype._write)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>createStream ()](#apidoc.element.seaport.protocol.prototype.createStream)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>destroy ()](#apidoc.element.seaport.protocol.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>send (row)](#apidoc.element.seaport.protocol.prototype.send)

#### [module seaport.seaport](#apidoc.module.seaport.seaport)
1.  [function <span class="apidocSignatureSpan">seaport.</span>seaport (opts)](#apidoc.element.seaport.seaport.seaport)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.</span>super ()](#apidoc.element.seaport.seaport.super)

#### [module seaport.seaport.prototype](#apidoc.module.seaport.seaport.prototype)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>_isAuthorized (id)](#apidoc.element.seaport.seaport.prototype._isAuthorized)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>close ()](#apidoc.element.seaport.seaport.prototype.close)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>createStream (addr)](#apidoc.element.seaport.seaport.prototype.createStream)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>free (meta)](#apidoc.element.seaport.seaport.prototype.free)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>get (meta, cb)](#apidoc.element.seaport.seaport.prototype.get)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>query (meta)](#apidoc.element.seaport.seaport.prototype.query)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>register ()](#apidoc.element.seaport.seaport.prototype.register)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>registerMeta (meta, port)](#apidoc.element.seaport.seaport.prototype.registerMeta)
1.  [function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>set (id, meta)](#apidoc.element.seaport.seaport.prototype.set)



# <a name="apidoc.module.seaport"></a>[module seaport](#apidoc.module.seaport)

#### <a name="apidoc.element.seaport.seaport"></a>[function <span class="apidocSignatureSpan"></span>seaport (opts)](#apidoc.element.seaport.seaport)
- description and source-code
```javascript
function Seaport(opts) {
    var self = this;
    if (!(this instanceof Seaport)) return new Seaport(opts);
    if (!opts) opts = {};
    this.endpoints = [];
    this.services = {};
    this.heartbeat = defined(opts.heartbeat, 15 * 1000);
    this.timeout = defined(opts.timeout, this.heartbeat * 3);
    this.known = {};
    this.doc = this; // for legacy .doc.set() syntax, deprecated

    if (opts.private) {
        var keys = { private: opts.private, public: opts.public };
        this.secure = secure(keys);
        if (opts.authorized) {
            this.authorized = opts.authorized.map(normalizeKey);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.connect"></a>[function <span class="apidocSignatureSpan">seaport.</span>connect ()](#apidoc.element.seaport.connect)
- description and source-code
```javascript
connect = function () {
    var args = [].slice.call(arguments);
    var opts = {};
    for (var i = 0; i < args.length; i++) {
        if (typeof args[i] === 'object') {
            opts = args[i];
            args.splice(i, 1);
            break;
        }
    }
    var port = args[0] || opts.port;
    var host = args[1] || opts.host;

    if (typeof port === 'string' && typeof host === 'number') {
        host = args[0];
        port = args[1];
    }
    if (typeof port === 'string' && /:\d+$/.test(port)) {
        host = port.split(':')[0];
        port = port.split(':')[1];
    }
    if (typeof port === 'string' && /^\d+$/.test(port)) {
        port = Number(port);
    }

    var s = seaport(opts);
    var conIx = 0;

    var c = (function reconnect () {
        if (s.closed) return;

        var hubs = [ { port : port, host : host } ].concat(s.query('seaport'));
        if (hubs.length <= conIx) conIx = hubs.length - 1;
        c = net.connect.call(null, hubs[conIx].port, hubs[conIx].host);
        conIx = (conIx + 1) % hubs.length;

        var active = true;

        c.on('connect', s.emit.bind(s, 'connect'));

        c.on('end', onend);
        c.on('error', onend);
        c.on('close', onend);

        var stream = s.createStream();
        stream.on('timeout', onend);

        c.pipe(stream).pipe(c);
        return c;

        function onend () {
            if (s.closed) return;
            if (!active) return;
            active = false;
            if (stream.destroy) stream.destroy();
            s.emit('disconnect');
            setTimeout(reconnect, 1000);
        }
    })();

    s.on('close', function () {
        if (c) c.end();
        if (nodeVersion !== '0.8') {
            if (c.destroy) c.destroy();
        }
    });

    return s;
}
```
- example usage
```shell
...

then obtain a port for a server called ''web'':

server.js:

''' js
var seaport = require('seaport');
var ports = seaport.connect('localhost', 9090);
var http = require('http');

var server = http.createServer(function (req, res) {
    res.end('beep boop\r\n');
});

server.listen(ports.register('web@1.2.3'));
...
```

#### <a name="apidoc.element.seaport.createServer"></a>[function <span class="apidocSignatureSpan">seaport.</span>createServer (opts)](#apidoc.element.seaport.createServer)
- description and source-code
```javascript
createServer = function (opts) {
    if (!opts) opts = {};
    opts.isServer = true;
    var s = seaport(opts);

    s.server = net.createServer(function (c) {
        c.on('error', function (error) {
            c.emit('end');
        });
        c.pipe(s.createStream(c.remoteAddress)).pipe(c);
    });
    s.listen = s.server.listen.bind(s.server);
    s.address = s.server.address.bind(s.server);

    s.peer = function () {
        if (!s.address()) {
            var args = arguments;
            s.once('listening', function () {
                s.peer.apply(s, args);
            });
            return;
        }
        var stream = s.createStream();
        var c = exports.connect.apply(this, arguments);
        s.on('close', c.close.bind(c));
        stream.pipe(c.createStream()).pipe(stream);

        c.register({
            role : 'seaport@' + version,
            port : s.address().port
        });
    };

    s.on('close', function () {
        s.server.close();
    });

    s.server.on('listening', s.emit.bind(s, 'listening'));
    s.server.on('connection', s.emit.bind(s, 'connection'));

    return s;
}
```
- example usage
```shell
...
};

exports.createServer = function (opts) {
if (!opts) opts = {};
opts.isServer = true;
var s = seaport(opts);

s.server = net.createServer(function (c) {
    c.on('error', function (error) {
        c.emit('end');
    });
    c.pipe(s.createStream(c.remoteAddress)).pipe(c);
});
s.listen = s.server.listen.bind(s.server);
s.address = s.server.address.bind(s.server);
...
```

#### <a name="apidoc.element.seaport.protocol"></a>[function <span class="apidocSignatureSpan">seaport.</span>protocol (opts)](#apidoc.element.seaport.protocol)
- description and source-code
```javascript
function Protocol(opts) {
    var self = this;
    if (!(self instanceof Protocol)) return new Protocol(opts);
    Duplex.call(self, { objectMode: true });
    if (!opts) opts = {};

    self.known = {};
    self.timing = {
        heartbeat: opts.heartbeat,
        timeout: opts.timeout
    };

    if (self.timing.heartbeat) {
        self.heartbeatInterval = setInterval(function () {
            self.send([ 'heartbeat' ]);
        }, self.timing.heartbeat);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.super"></a>[function <span class="apidocSignatureSpan">seaport.</span>super ()](#apidoc.element.seaport.super)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.seaport.protocol"></a>[module seaport.protocol](#apidoc.module.seaport.protocol)

#### <a name="apidoc.element.seaport.protocol.protocol"></a>[function <span class="apidocSignatureSpan">seaport.</span>protocol (opts)](#apidoc.element.seaport.protocol.protocol)
- description and source-code
```javascript
function Protocol(opts) {
    var self = this;
    if (!(self instanceof Protocol)) return new Protocol(opts);
    Duplex.call(self, { objectMode: true });
    if (!opts) opts = {};

    self.known = {};
    self.timing = {
        heartbeat: opts.heartbeat,
        timeout: opts.timeout
    };

    if (self.timing.heartbeat) {
        self.heartbeatInterval = setInterval(function () {
            self.send([ 'heartbeat' ]);
        }, self.timing.heartbeat);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.protocol.super"></a>[function <span class="apidocSignatureSpan">seaport.protocol.</span>super (options)](#apidoc.element.seaport.protocol.super)
- description and source-code
```javascript
function Duplex(options) {
  if (!(this instanceof Duplex))
    return new Duplex(options);

  Readable.call(this, options);
  Writable.call(this, options);

  if (options && options.readable === false)
    this.readable = false;

  if (options && options.writable === false)
    this.writable = false;

  this.allowHalfOpen = true;
  if (options && options.allowHalfOpen === false)
    this.allowHalfOpen = false;

  this.once('end', onend);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.seaport.protocol.prototype"></a>[module seaport.protocol.prototype](#apidoc.module.seaport.protocol.prototype)

#### <a name="apidoc.element.seaport.protocol.prototype._read"></a>[function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>_read (size)](#apidoc.element.seaport.protocol.prototype._read)
- description and source-code
```javascript
_read = function (size) {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.protocol.prototype._write"></a>[function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>_write (row, enc, next)](#apidoc.element.seaport.protocol.prototype._write)
- description and source-code
```javascript
_write = function (row, enc, next) {
    var self = this;
    if (row[0] === 'register') {
        this.known[row[1]] = row[2];
        this.emit('register', row[1], row[2]);
    }
    else if (row[0] === 'free') {
        var meta = this.known[row[1]];
        delete this.known[row[1]];
        this.emit('free', row[1], meta);
    }
    else if (row[0] === 'helo') {
        this.emit('helo', row[1]);
    }
    else if (row[0] === 'heartbeat') {
        this.emit('heartbeat');
        if (this.timing.timeout) {
            clearTimeout(this.timeout);
            this.timeout = setTimeout(function () {
                self.emit('timeout');
            }, this.timing.timeout);
        }
    }
    else if (row[0] === 'synced') {
        this.emit('synced');
    }
    next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.protocol.prototype.createStream"></a>[function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>createStream ()](#apidoc.element.seaport.protocol.prototype.createStream)
- description and source-code
```javascript
createStream = function () {
    var unsplit = through(function (row) {
        this.queue(json.stringify(row) + '\n');
    });
    return combine(split(json.parse), this, unsplit);
}
```
- example usage
```shell
...

c.on('connect', s.emit.bind(s, 'connect'));

c.on('end', onend);
c.on('error', onend);
c.on('close', onend);

var stream = s.createStream();
stream.on('timeout', onend);

c.pipe(stream).pipe(c);
return c;

function onend () {
    if (s.closed) return;
...
```

#### <a name="apidoc.element.seaport.protocol.prototype.destroy"></a>[function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>destroy ()](#apidoc.element.seaport.protocol.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
    clearInterval(this.heartbeatInterval);
    clearTimeout(this.timeout);
}
```
- example usage
```shell
...
    c.pipe(stream).pipe(c);
    return c;

    function onend () {
        if (s.closed) return;
        if (!active) return;
        active = false;
        if (stream.destroy) stream.destroy();
        s.emit('disconnect');
        setTimeout(reconnect, 1000);
    }
})();

s.on('close', function () {
    if (c) c.end();
...
```

#### <a name="apidoc.element.seaport.protocol.prototype.send"></a>[function <span class="apidocSignatureSpan">seaport.protocol.prototype.</span>send (row)](#apidoc.element.seaport.protocol.prototype.send)
- description and source-code
```javascript
send = function (row) {
    this.push(row);
}
```
- example usage
```shell
...
    self.timing = {
        heartbeat: opts.heartbeat,
        timeout: opts.timeout
    };

    if (self.timing.heartbeat) {
        self.heartbeatInterval = setInterval(function () {
            self.send([ 'heartbeat' ]);
        }, self.timing.heartbeat);
    }
}

Protocol.prototype.send = function (row) {
    this.push(row);
};
...
```



# <a name="apidoc.module.seaport.seaport"></a>[module seaport.seaport](#apidoc.module.seaport.seaport)

#### <a name="apidoc.element.seaport.seaport.seaport"></a>[function <span class="apidocSignatureSpan">seaport.</span>seaport (opts)](#apidoc.element.seaport.seaport.seaport)
- description and source-code
```javascript
function Seaport(opts) {
    var self = this;
    if (!(this instanceof Seaport)) return new Seaport(opts);
    if (!opts) opts = {};
    this.endpoints = [];
    this.services = {};
    this.heartbeat = defined(opts.heartbeat, 15 * 1000);
    this.timeout = defined(opts.timeout, this.heartbeat * 3);
    this.known = {};
    this.doc = this; // for legacy .doc.set() syntax, deprecated

    if (opts.private) {
        var keys = { private: opts.private, public: opts.public };
        this.secure = secure(keys);
        if (opts.authorized) {
            this.authorized = opts.authorized.map(normalizeKey);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.seaport.seaport.super"></a>[function <span class="apidocSignatureSpan">seaport.seaport.</span>super ()](#apidoc.element.seaport.seaport.super)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.seaport.seaport.prototype"></a>[module seaport.seaport.prototype](#apidoc.module.seaport.seaport.prototype)

#### <a name="apidoc.element.seaport.seaport.prototype._isAuthorized"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>_isAuthorized (id)](#apidoc.element.seaport.seaport.prototype._isAuthorized)
- description and source-code
```javascript
_isAuthorized = function (id) {
    if (!this.authorized) return true;
    return indexOf(this.authorized, normalizeKey(id)) >= 0;
}
```
- example usage
```shell
...
this.emit('endpoint', p);
var stream;
if (this.secure) {
    stream = this.secure(function (s) {
        s.pipe(p.createStream()).pipe(s);
    });
    stream.on('identify', function (id) {
        if (self._isAuthorized(id.key.public)) {
            id.accept();
            self.emit('accept', id);
        }
        else {
            id.reject();
            self.emit('reject', id);
        }
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.close"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>close ()](#apidoc.element.seaport.seaport.prototype.close)
- description and source-code
```javascript
close = function () {
    this.closed = true;
    for (var i = 0; i < this.endpoints.length; i++) {
        var e = this.endpoints[i];
        e.emit('close');
        e.end();
    }
    this.emit('close');
}
```
- example usage
```shell
...
        c.register({
            role : 'seaport@' + version,
            port : s.address().port
        });
    };

    s.on('close', function () {
        s.server.close();
    });

    s.server.on('listening', s.emit.bind(s, 'listening'));
    s.server.on('connection', s.emit.bind(s, 'connection'));

    return s;
};
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.createStream"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>createStream (addr)](#apidoc.element.seaport.seaport.prototype.createStream)
- description and source-code
```javascript
createStream = function (addr) {
    var self = this;
    var p = new Protocol({
        heartbeat: this.heartbeat,
        timeout: this.timeout,
    });
    this.endpoints.push(p);

    p.on('end', onend);
    p.on('register', function onregister (id, meta) {
        // prevents loops when peers connect from both sides
        if (self.known[id] && self.query(meta).length) return;

        if (!meta.host) meta.host = self._host;

        if (self.services[id]) {
            self.services[id] = meta;
        }
        else {
            self.known[id] = meta;
        }

        for (var i = 0; i < self.endpoints.length; i++) {
            var e = self.endpoints[i];
            if (e === p) continue;
            e.send([ 'register', id, meta ]);
        }
        self.emit('register', meta, id);
    });
    p.on('timeout', function () {
        onend();
        stream.emit('timeout');
    });
    p.on('free', function (id) {
        var obj = self.known[id] ? self.known : self.services;
        var meta = obj[id];
        if (!meta) return;

        for (var i = 0; i < self.endpoints.length; i++) {
            var e = self.endpoints[i];
            e.send(['free', id]);
        }

        delete obj[id];
        self.emit('free', meta, id);
    });
    p.on('synced', function () {
        stream.emit('synced');
        self.emit('synced', stream);
    });

    if (!addr && !self._host) {
        p.on('helo', function (addr) {
            self._host = addr;
            self.emit('address', addr);
        });
    }

    this.emit('endpoint', p);
    var stream;
    if (this.secure) {
        stream = this.secure(function (s) {
            s.pipe(p.createStream()).pipe(s);
        });
        stream.on('identify', function (id) {
            if (self._isAuthorized(id.key.public)) {
                id.accept();
                self.emit('accept', id);
            }
            else {
                id.reject();
                self.emit('reject', id);
            }
        });
    }
    else {
        stream = p.createStream();
    }
    stream.on('error', onend);
    stream.on('close', onend);
    p.once('close', function () {
        p.destroy();
        var keys = objectKeys(p.known);
        for (var i = 0; i < keys.length; i++) {
            var key = keys[i];
            var meta = self.known[key];
            if (!meta) continue;
            delete self.known[key];
            self.emit('free', meta, key);
        }
    });

    if (addr) p.send([ 'helo', addr ]);

    registerServices(merge(this.known, this.services), p);
    self.emit('stream', stream);
    self.emit('protocol', p);
    return stream;

    function onend () {
        if (p._ended) return;
        p._ended = true;
        p.destroy();

        var ix = indexOf(self.endpoints, p);
        self.endpoints.splice(ix, 1);
        var keys = objectKeys(p.known);
        for (var i = 0; i < keys.length; i++) {
            var key = keys[i];
            var meta = self.known[key];
            if (!meta) continue;

            delete self.known[key];

            for (var j = 0; j < self.endpoints.length; j++) {
                var e = self.endpoints[j];
                if (e === p) continue;
                e.send([ 'free', key ]);
            }

            self.emit('free', meta, key);
        }
    }
}
```
- example usage
```shell
...

c.on('connect', s.emit.bind(s, 'connect'));

c.on('end', onend);
c.on('error', onend);
c.on('close', onend);

var stream = s.createStream();
stream.on('timeout', onend);

c.pipe(stream).pipe(c);
return c;

function onend () {
    if (s.closed) return;
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.free"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>free (meta)](#apidoc.element.seaport.seaport.prototype.free)
- description and source-code
```javascript
free = function (meta) {
    var id;
    if (typeof meta === 'number') {
        meta = { port: meta };
    }
    if (typeof meta === 'object') {
        var keys = objectKeys(this.services).concat(objectKeys(this.known));
        var mkeys = objectKeys(meta);
        for (var i = 0; i < keys.length; i++) {
            var s = this.services[keys[i]] || this.known[keys[i]];
            for (var j = 0; j < mkeys.length; j++) {
                if (meta[mkeys[j]] !== s[mkeys[j]]) break;
            }
            if (j === mkeys.length) {
                id = keys[i];
                meta = this.services[id];
                break;
            }
        }
        if (i === keys.length) return;
    }
    else {
        id = meta;
        meta = this.services[id] || this.known[id];
    }

    if (this.services[id]) {
        meta = this.services[id];
        delete this.services[id];
    } else if (this.known[id]) {
        meta = this.known[id];
        delete this.known[id];
    } else {
        return;
    }

    for (var i = 0; i < this.endpoints.length; i++) {
        var e = this.endpoints[i];
        e.send([ 'free', id ]);
    }
    this.emit('free', meta, id);
}
```
- example usage
```shell
...

## s.get(role, cb)

Like '.query()', but does 'cb(services)' with the list of matching entries.
If 'services' is empty, 'cb' won't fire until there is at least one match
available.

## s.free(service), s.free(id)

Remove a service registered with '.register()'. You can remove a service by the
'service' object itself or just its 'id'.

## s.authorize(publicKey)

Authorize the PEM-encoded 'publicKey' string to make updates.
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.get"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>get (meta, cb)](#apidoc.element.seaport.seaport.prototype.get)
- description and source-code
```javascript
function get(meta, cb) {
    var self = this;
    var ps = this.query(meta);
    if (ps.length > 0) return cb(ps);
    this.once('register', function () { self.get(meta, cb) });
}
```
- example usage
```shell
...
client.js:

''' js
var seaport = require('seaport');
var ports = seaport.connect(9090);
var request = require('request');

ports.get('web@1.2.x', function (ps) {
    var u = 'http://' + ps[0].host + ':' + ps[0].port;
    request(u).pipe(process.stdout);
});
'''

output:
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.query"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>query (meta)](#apidoc.element.seaport.seaport.prototype.query)
- description and source-code
```javascript
query = function (meta) {
    meta = fixMeta(meta);
    var mkeys = objectKeys(meta);
    var skeys = objectKeys(this.services);
    var keys = objectKeys(this.known);

    var rows = [];
    for (var i = 0; i < keys.length; i++) {
        var key = keys[i];
        var row = this.known[key];
        if (matches(row)) rows.push(row);
    }
    for (var i = 0; i < skeys.length; i++) {
        var key = skeys[i];
        var row = this.services[key];
        if (matches(row)) rows.push(row);
    }
    return rows;

    function matches (row) {
        for (var i = 0; i < mkeys.length; i++) {
            var mkey = mkeys[i];
            if (mkey === 'version') {
                if (!semver.satisfies(row.version, meta.version)) {
                    return false;
                }
            }
            else if (row[mkey] !== meta[mkey]) return false;
        }
        return true;
    }
}
```
- example usage
```shell
...

var s = seaport(opts);
var conIx = 0;

var c = (function reconnect () {
    if (s.closed) return;

    var hubs = [ { port : port, host : host } ].concat(s.query('seaport'));
    if (hubs.length <= conIx) conIx = hubs.length - 1;
    c = net.connect.call(null, hubs[conIx].port, hubs[conIx].host);
    conIx = (conIx + 1) % hubs.length;

    var active = true;

    c.on('connect', s.emit.bind(s, 'connect'));
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.register"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>register ()](#apidoc.element.seaport.seaport.prototype.register)
- description and source-code
```javascript
register = function () {
    return this.registerMeta.apply(this, arguments).port;
}
```
- example usage
```shell
...
        return;
    }
    var stream = s.createStream();
    var c = exports.connect.apply(this, arguments);
    s.on('close', c.close.bind(c));
    stream.pipe(c.createStream()).pipe(stream);

    c.register({
        role : 'seaport@' + version,
        port : s.address().port
    });
};

s.on('close', function () {
    s.server.close();
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.registerMeta"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>registerMeta (meta, port)](#apidoc.element.seaport.seaport.prototype.registerMeta)
- description and source-code
```javascript
registerMeta = function (meta, port) {
    var self = this;
    meta = fixMeta(meta, port);

    if (!meta.port) {
        meta.port = 10000 + Math.floor(Math.random() * 55000);
    }
    var id = meta.id || generateId();
    meta.id = id;
    this.services[id] = meta;

    if (!meta.host && this._host) {
        meta.host = this._host;
        register();
    }
    else if (!meta.host) {
        this.once('address', function (addr) {
            meta.host = addr;
            register();
        });
    }
    else register()

    return meta;

    function register () {
        var mserv = {};
        mserv[id] = meta;
        for (var i = 0; i < self.endpoints.length; i++) {
            registerServices(mserv, self.endpoints[i]);
        }
    }
}
```
- example usage
```shell
...

If you don't want you specify 'role' you can also use 'opts.role' and
'opts.version'.

You can control what the key name will be by setting 'opts.id' yourself.
Otherwise a random hex string will be used.

## var meta = s.registerMeta(role, opts)

Like 's.register()', but return the entire meta object instead of just the
'meta.port'. This is handy if you need the 'id' to update metadata later.

## var services = s.query(search)

Query the seaport entries with 'search' as a 'name@semver' string.
...
```

#### <a name="apidoc.element.seaport.seaport.prototype.set"></a>[function <span class="apidocSignatureSpan">seaport.seaport.prototype.</span>set (id, meta)](#apidoc.element.seaport.seaport.prototype.set)
- description and source-code
```javascript
set = function (id, meta) {
    var records = this.services[id] ? this.services : this.known;
    if (!records[id]) return;

    records[id] = meta;
    if (this.services[id]) return;

    for (var i = 0; i < this.endpoints.length; i++) {
        var e = this.endpoints[i];
        e.send([ 'register', id, meta ]);
    }
}
```
- example usage
```shell
...
Authorize the PEM-encoded 'publicKey' string to make updates.
Updates include registering services and setting keys.

## s.close()

Close a seaport connection or server. Cancel any pending requests.

## s.set(id, value)

Update a registration value by its 'id', broadcasting the new registration meta
'value'.

# events

## s.on('register', function (service) {})
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
