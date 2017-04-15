# api documentation for  [webtorrent (v0.98.18)](https://webtorrent.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-webtorrent.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webtorrent) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webtorrent.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webtorrent)
#### Streaming torrent client

[![NPM](https://nodei.co/npm/webtorrent.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/webtorrent)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webtorrent/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "WebTorrent, LLC",
        "url": "https://webtorrent.io"
    },
    "browser": {
        "./lib/server.js": false,
        "./lib/tcp-pool.js": false,
        "bittorrent-dht/client": false,
        "fs-chunk-store": "memory-chunk-store",
        "load-ip-set": false,
        "net": false,
        "os": false,
        "ut_pex": false
    },
    "browserify": {
        "transform": [
            "package-json-versionify"
        ]
    },
    "bugs": {
        "url": "https://github.com/webtorrent/webtorrent/issues"
    },
    "dependencies": {
        "addr-to-ip-port": "^1.4.2",
        "bitfield": "^1.1.2",
        "bittorrent-dht": "^7.2.2",
        "bittorrent-protocol": "^2.1.5",
        "chunk-store-stream": "^2.0.2",
        "create-torrent": "^3.24.5",
        "debug": "^2.2.0",
        "end-of-stream": "^1.1.0",
        "fs-chunk-store": "^1.6.2",
        "immediate-chunk-store": "^1.0.8",
        "inherits": "^2.0.1",
        "load-ip-set": "^1.2.7",
        "memory-chunk-store": "^1.2.0",
        "mime": "^1.3.4",
        "multistream": "^2.0.5",
        "package-json-versionify": "^1.0.2",
        "parse-torrent": "^5.8.0",
        "pump": "^1.0.1",
        "random-iterate": "^1.0.1",
        "randombytes": "^2.0.3",
        "range-parser": "^1.2.0",
        "readable-stream": "^2.1.4",
        "render-media": "^2.8.0",
        "run-parallel": "^1.1.6",
        "run-parallel-limit": "^1.0.3",
        "safe-buffer": "^5.0.1",
        "simple-concat": "^1.0.0",
        "simple-get": "^2.2.1",
        "simple-peer": "^8.0.0",
        "simple-sha1": "^2.0.8",
        "speedometer": "^1.0.0",
        "stream-to-blob": "^1.0.0",
        "stream-to-blob-url": "^2.1.0",
        "stream-with-known-length-to-buffer": "^1.0.0",
        "torrent-discovery": "^8.1.0",
        "torrent-piece": "^1.1.0",
        "uniq": "^1.0.1",
        "unordered-array-remove": "^1.0.2",
        "ut_metadata": "^3.0.8",
        "ut_pex": "^1.1.1",
        "xtend": "^4.0.1",
        "zero-fill": "^2.2.3"
    },
    "description": "Streaming torrent client",
    "devDependencies": {
        "bittorrent-tracker": "^9.0.0",
        "brfs": "^1.4.3",
        "browserify": "^14.0.0",
        "cross-spawn": "^5.0.1",
        "electron-prebuilt": "^0.37.8",
        "finalhandler": "^1.0.0",
        "network-address": "^1.1.0",
        "run-series": "^1.1.4",
        "serve-static": "^1.11.1",
        "standard": "*",
        "tape": "^4.6.0",
        "uglify-js": "^2.7.0",
        "webtorrent-fixtures": "^1.5.0",
        "zuul": "^3.10.1"
    },
    "directories": {},
    "dist": {
        "shasum": "d8e0e04a52af884e9cffa361cbe8c159a4cb6f98",
        "tarball": "https://registry.npmjs.org/webtorrent/-/webtorrent-0.98.18.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "eb7ef40d80ebf7fa29188efe0580f2b0c5f3c95c",
    "homepage": "https://webtorrent.io",
    "keywords": [
        "bittorrent",
        "bittorrent client",
        "download",
        "mad science",
        "p2p",
        "peer-to-peer",
        "peers",
        "streaming",
        "swarm",
        "torrent",
        "web torrent",
        "webrtc",
        "webrtc data",
        "webtorrent"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "feross"
        }
    ],
    "name": "webtorrent",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/webtorrent/webtorrent.git"
    },
    "scripts": {
        "build": "browserify -s WebTorrent -e ./ | uglifyjs -c warnings=false -m > webtorrent.min.js",
        "build-debug": "browserify -s WebTorrent -e ./ > webtorrent.debug.js",
        "size": "npm run build && cat webtorrent.min.js | gzip | wc -c",
        "test": "standard && node ./bin/test.js",
        "test-browser": "zuul -- test/*.js test/browser/*.js",
        "test-browser-headless": "zuul --electron -- test/*.js test/browser/*.js",
        "test-browser-local": "zuul --local -- test/*.js test/browser/*.js",
        "test-node": "tape test/*.js test/node/*.js",
        "update-authors": "./bin/update-authors.sh"
    },
    "version": "0.98.18"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webtorrent](#apidoc.module.webtorrent)
1.  boolean <span class="apidocSignatureSpan">webtorrent.</span>WEBRTC_SUPPORT
1.  [function <span class="apidocSignatureSpan"></span>webtorrent (opts)](#apidoc.element.webtorrent.webtorrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>super_ ()](#apidoc.element.webtorrent.super_)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>toString ()](#apidoc.element.webtorrent.toString)



# <a name="apidoc.module.webtorrent"></a>[module webtorrent](#apidoc.module.webtorrent)

#### <a name="apidoc.element.webtorrent.webtorrent"></a>[function <span class="apidocSignatureSpan"></span>webtorrent (opts)](#apidoc.element.webtorrent.webtorrent)
- description and source-code
```javascript
function WebTorrent(opts) {
  var self = this
  if (!(self instanceof WebTorrent)) return new WebTorrent(opts)
  EventEmitter.call(self)

  if (!opts) opts = {}

  if (typeof opts.peerId === 'string') {
    self.peerId = opts.peerId
  } else if (Buffer.isBuffer(opts.peerId)) {
    self.peerId = opts.peerId.toString('hex')
  } else {
    self.peerId = Buffer.from(VERSION_PREFIX + randombytes(9).toString('base64')).toString('hex')
  }
  self.peerIdBuffer = Buffer.from(self.peerId, 'hex')

  if (typeof opts.nodeId === 'string') {
    self.nodeId = opts.nodeId
  } else if (Buffer.isBuffer(opts.nodeId)) {
    self.nodeId = opts.nodeId.toString('hex')
  } else {
    self.nodeId = randombytes(20).toString('hex')
  }
  self.nodeIdBuffer = Buffer.from(self.nodeId, 'hex')

  self._debugId = self.peerId.toString('hex').substring(0, 7)

  self.destroyed = false
  self.listening = false
  self.torrentPort = opts.torrentPort || 0
  self.dhtPort = opts.dhtPort || 0
  self.tracker = opts.tracker !== undefined ? opts.tracker : {}
  self.torrents = []
  self.maxConns = Number(opts.maxConns) || 55

  self._debug(
    'new webtorrent (peerId %s, nodeId %s, port %s)',
    self.peerId, self.nodeId, self.torrentPort
  )

  if (self.tracker) {
    if (typeof self.tracker !== 'object') self.tracker = {}
    if (opts.rtcConfig) {
      // TODO: remove in v1
      console.warn('WebTorrent: opts.rtcConfig is deprecated. Use opts.tracker.rtcConfig instead')
      self.tracker.rtcConfig = opts.rtcConfig
    }
    if (opts.wrtc) {
      // TODO: remove in v1
      console.warn('WebTorrent: opts.wrtc is deprecated. Use opts.tracker.wrtc instead')
      self.tracker.wrtc = opts.wrtc
    }
    if (global.WRTC && !self.tracker.wrtc) {
      self.tracker.wrtc = global.WRTC
    }
  }

  if (typeof TCPPool === 'function') {
    self._tcpPool = new TCPPool(self)
  } else {
    process.nextTick(function () {
      self._onListening()
    })
  }

  // stats
  self._downloadSpeed = speedometer()
  self._uploadSpeed = speedometer()

  if (opts.dht !== false && typeof DHT === 'function' /* browser exclude */) {
    // use a single DHT instance for all torrents, so the routing table can be reused
    self.dht = new DHT(extend({ nodeId: self.nodeId }, opts.dht))

    self.dht.once('error', function (err) {
      self._destroy(err)
    })

    self.dht.once('listening', function () {
      var address = self.dht.address()
      if (address) self.dhtPort = address.port
    })

    // Ignore warning when there are > 10 torrents in the client
    self.dht.setMaxListeners(0)

    self.dht.listen(self.dhtPort)
  } else {
    self.dht = false
  }

  // Enable or disable BEP19 (Web Seeds). Enabled by default:
  self.enableWebSeeds = opts.webSeeds !== false

  if (typeof loadIPSet === 'function' && opts.blocklist != null) {
    loadIPSet(opts.blocklist, {
      headers: {
        'user-agent': 'WebTorrent/' + VERSION + ' (https://webtorrent.io)'
      }
    }, function (err, ipSet) {
      if (err) return self.error('Failed to load blocklist: ' + err.message)
      self.blocked = ipSet
      ready()
    })
  } else {
    process.nextTick(ready)
  }

  function ready () {
    if (self.destroyed) return
    self.ready = true
    self.emit('ready')
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.super_"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>super_ ()](#apidoc.element.webtorrent.super_)
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

#### <a name="apidoc.element.webtorrent.toString"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>toString ()](#apidoc.element.webtorrent.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
...
EventEmitter.call(self)

if (!opts) opts = {}

if (typeof opts.peerId === 'string') {
  self.peerId = opts.peerId
} else if (Buffer.isBuffer(opts.peerId)) {
  self.peerId = opts.peerId.toString('hex')
} else {
  self.peerId = Buffer.from(VERSION_PREFIX + randombytes(9).toString('base64')).toString('hex')
}
self.peerIdBuffer = Buffer.from(self.peerId, 'hex')

if (typeof opts.nodeId === 'string') {
  self.nodeId = opts.nodeId
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
