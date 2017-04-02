# api documentation for  [webtorrent (v0.98.15)](https://webtorrent.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-webtorrent.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webtorrent) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webtorrent.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webtorrent)
#### Streaming torrent client

[![NPM](https://nodei.co/npm/webtorrent.png?downloads=true)](https://www.npmjs.com/package/webtorrent)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webtorrent_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webtorrent/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "WebTorrent, LLC",
        "email": "feross@webtorrent.io",
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
        "url": "https://github.com/feross/webtorrent/issues"
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
        "simple-peer": "^7.0.0",
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
        "shasum": "db07e6e82269935f5d3855ca71be00dff8b38efb",
        "tarball": "https://registry.npmjs.org/webtorrent/-/webtorrent-0.98.15.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "5051d8f5a74d4d6e09ab19d9d9849d0c7d960651",
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
            "name": "feross",
            "email": "feross@feross.org"
        }
    ],
    "name": "webtorrent",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/feross/webtorrent.git"
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
    "version": "0.98.15"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webtorrent](#apidoc.module.webtorrent)
1.  boolean <span class="apidocSignatureSpan">webtorrent.</span>WEBRTC_SUPPORT
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>file (torrent, file)](#apidoc.element.webtorrent.file)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>file_stream (file, opts)](#apidoc.element.webtorrent.file_stream)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>rarity_map (torrent)](#apidoc.element.webtorrent.rarity_map)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>super_ ()](#apidoc.element.webtorrent.super_)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>tcp_pool (client)](#apidoc.element.webtorrent.tcp_pool)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>torrent (torrentId, client, opts)](#apidoc.element.webtorrent.torrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>webconn (url, torrent)](#apidoc.element.webtorrent.webconn)
1.  object <span class="apidocSignatureSpan">webtorrent.</span>file.prototype
1.  object <span class="apidocSignatureSpan">webtorrent.</span>file_stream.prototype
1.  object <span class="apidocSignatureSpan">webtorrent.</span>peer
1.  object <span class="apidocSignatureSpan">webtorrent.</span>rarity_map.prototype
1.  object <span class="apidocSignatureSpan">webtorrent.</span>tcp_pool.prototype
1.  object <span class="apidocSignatureSpan">webtorrent.</span>torrent.prototype
1.  object <span class="apidocSignatureSpan">webtorrent.</span>webconn.prototype

#### [module webtorrent.file](#apidoc.module.webtorrent.file)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>file (torrent, file)](#apidoc.element.webtorrent.file.file)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.</span>super_ ()](#apidoc.element.webtorrent.file.super_)

#### [module webtorrent.file.prototype](#apidoc.module.webtorrent.file.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>_destroy ()](#apidoc.element.webtorrent.file.prototype._destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>_getMimeType ()](#apidoc.element.webtorrent.file.prototype._getMimeType)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>appendTo (elem, opts, cb)](#apidoc.element.webtorrent.file.prototype.appendTo)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>createReadStream (opts)](#apidoc.element.webtorrent.file.prototype.createReadStream)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>deselect ()](#apidoc.element.webtorrent.file.prototype.deselect)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBlob (cb)](#apidoc.element.webtorrent.file.prototype.getBlob)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBlobURL (cb)](#apidoc.element.webtorrent.file.prototype.getBlobURL)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBuffer (cb)](#apidoc.element.webtorrent.file.prototype.getBuffer)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>renderTo (elem, opts, cb)](#apidoc.element.webtorrent.file.prototype.renderTo)
1.  [function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>select (priority)](#apidoc.element.webtorrent.file.prototype.select)

#### [module webtorrent.file_stream](#apidoc.module.webtorrent.file_stream)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>file_stream (file, opts)](#apidoc.element.webtorrent.file_stream.file_stream)
1.  [function <span class="apidocSignatureSpan">webtorrent.file_stream.</span>super_ (options)](#apidoc.element.webtorrent.file_stream.super_)

#### [module webtorrent.file_stream.prototype](#apidoc.module.webtorrent.file_stream.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_destroy (err, onclose)](#apidoc.element.webtorrent.file_stream.prototype._destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_notify ()](#apidoc.element.webtorrent.file_stream.prototype._notify)
1.  [function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_read ()](#apidoc.element.webtorrent.file_stream.prototype._read)
1.  [function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>destroy (onclose)](#apidoc.element.webtorrent.file_stream.prototype.destroy)

#### [module webtorrent.peer](#apidoc.module.webtorrent.peer)
1.  [function <span class="apidocSignatureSpan">webtorrent.peer.</span>createTCPIncomingPeer (conn)](#apidoc.element.webtorrent.peer.createTCPIncomingPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.peer.</span>createTCPOutgoingPeer (addr, swarm)](#apidoc.element.webtorrent.peer.createTCPOutgoingPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.peer.</span>createWebRTCPeer (conn, swarm)](#apidoc.element.webtorrent.peer.createWebRTCPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.peer.</span>createWebSeedPeer (url, swarm)](#apidoc.element.webtorrent.peer.createWebSeedPeer)

#### [module webtorrent.rarity_map](#apidoc.module.webtorrent.rarity_map)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>rarity_map (torrent)](#apidoc.element.webtorrent.rarity_map.rarity_map)

#### [module webtorrent.rarity_map.prototype](#apidoc.module.webtorrent.rarity_map.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>_cleanupWireEvents (wire)](#apidoc.element.webtorrent.rarity_map.prototype._cleanupWireEvents)
1.  [function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>_initWire (wire)](#apidoc.element.webtorrent.rarity_map.prototype._initWire)
1.  [function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>destroy ()](#apidoc.element.webtorrent.rarity_map.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>getRarestPiece (pieceFilterFunc)](#apidoc.element.webtorrent.rarity_map.prototype.getRarestPiece)
1.  [function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>recalculate ()](#apidoc.element.webtorrent.rarity_map.prototype.recalculate)

#### [module webtorrent.tcp_pool](#apidoc.module.webtorrent.tcp_pool)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>tcp_pool (client)](#apidoc.element.webtorrent.tcp_pool.tcp_pool)

#### [module webtorrent.tcp_pool.prototype](#apidoc.module.webtorrent.tcp_pool.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.tcp_pool.prototype.</span>_onConnection (conn)](#apidoc.element.webtorrent.tcp_pool.prototype._onConnection)
1.  [function <span class="apidocSignatureSpan">webtorrent.tcp_pool.prototype.</span>destroy (cb)](#apidoc.element.webtorrent.tcp_pool.prototype.destroy)

#### [module webtorrent.torrent](#apidoc.module.webtorrent.torrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>torrent (torrentId, client, opts)](#apidoc.element.webtorrent.torrent.torrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.</span>super_ ()](#apidoc.element.webtorrent.torrent.super_)

#### [module webtorrent.torrent.prototype](#apidoc.module.webtorrent.torrent.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_addIncomingPeer (peer)](#apidoc.element.webtorrent.torrent.prototype._addIncomingPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_addPeer (peer)](#apidoc.element.webtorrent.torrent.prototype._addPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_checkDone ()](#apidoc.element.webtorrent.torrent.prototype._checkDone)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_debug ()](#apidoc.element.webtorrent.torrent.prototype._debug)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_destroy (err, cb)](#apidoc.element.webtorrent.torrent.prototype._destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_drain ()](#apidoc.element.webtorrent.torrent.prototype._drain)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_gcSelections ()](#apidoc.element.webtorrent.torrent.prototype._gcSelections)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_getMetadataFromServer ()](#apidoc.element.webtorrent.torrent.prototype._getMetadataFromServer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_hotswap (wire, index)](#apidoc.element.webtorrent.torrent.prototype._hotswap)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_markVerified (index)](#apidoc.element.webtorrent.torrent.prototype._markVerified)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onListening ()](#apidoc.element.webtorrent.torrent.prototype._onListening)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onMetadata (metadata)](#apidoc.element.webtorrent.torrent.prototype._onMetadata)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onParsedTorrent (parsedTorrent)](#apidoc.element.webtorrent.torrent.prototype._onParsedTorrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onStore ()](#apidoc.element.webtorrent.torrent.prototype._onStore)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onTorrentId (torrentId)](#apidoc.element.webtorrent.torrent.prototype._onTorrentId)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onWire (wire, addr)](#apidoc.element.webtorrent.torrent.prototype._onWire)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onWireWithMetadata (wire)](#apidoc.element.webtorrent.torrent.prototype._onWireWithMetadata)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_processParsedTorrent (parsedTorrent)](#apidoc.element.webtorrent.torrent.prototype._processParsedTorrent)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_rechoke ()](#apidoc.element.webtorrent.torrent.prototype._rechoke)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_request (wire, index, hotswap)](#apidoc.element.webtorrent.torrent.prototype._request)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_update ()](#apidoc.element.webtorrent.torrent.prototype._update)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateInterest ()](#apidoc.element.webtorrent.torrent.prototype._updateInterest)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateSelections ()](#apidoc.element.webtorrent.torrent.prototype._updateSelections)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateWire (wire)](#apidoc.element.webtorrent.torrent.prototype._updateWire)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_validAddr (addr)](#apidoc.element.webtorrent.torrent.prototype._validAddr)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_verifyPieces ()](#apidoc.element.webtorrent.torrent.prototype._verifyPieces)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>addPeer (peer)](#apidoc.element.webtorrent.torrent.prototype.addPeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>addWebSeed (url)](#apidoc.element.webtorrent.torrent.prototype.addWebSeed)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>createServer (requestListener)](#apidoc.element.webtorrent.torrent.prototype.createServer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>critical (start, end)](#apidoc.element.webtorrent.torrent.prototype.critical)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>deselect (start, end, priority)](#apidoc.element.webtorrent.torrent.prototype.deselect)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>destroy (cb)](#apidoc.element.webtorrent.torrent.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>getFileModtimes (cb)](#apidoc.element.webtorrent.torrent.prototype.getFileModtimes)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>load (streams, cb)](#apidoc.element.webtorrent.torrent.prototype.load)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>pause ()](#apidoc.element.webtorrent.torrent.prototype.pause)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>removePeer (peer)](#apidoc.element.webtorrent.torrent.prototype.removePeer)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>resume ()](#apidoc.element.webtorrent.torrent.prototype.resume)
1.  [function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>select (start, end, priority, notify)](#apidoc.element.webtorrent.torrent.prototype.select)

#### [module webtorrent.webconn](#apidoc.module.webtorrent.webconn)
1.  [function <span class="apidocSignatureSpan">webtorrent.</span>webconn (url, torrent)](#apidoc.element.webtorrent.webconn.webconn)
1.  [function <span class="apidocSignatureSpan">webtorrent.webconn.</span>super_ ()](#apidoc.element.webtorrent.webconn.super_)

#### [module webtorrent.webconn.prototype](#apidoc.module.webtorrent.webconn.prototype)
1.  [function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>_init ()](#apidoc.element.webtorrent.webconn.prototype._init)
1.  [function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>destroy ()](#apidoc.element.webtorrent.webconn.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>httpRequest (pieceIndex, offset, length, cb)](#apidoc.element.webtorrent.webconn.prototype.httpRequest)



# <a name="apidoc.module.webtorrent"></a>[module webtorrent](#apidoc.module.webtorrent)

#### <a name="apidoc.element.webtorrent.file"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>file (torrent, file)](#apidoc.element.webtorrent.file)
- description and source-code
```javascript
function File(torrent, file) {
  EventEmitter.call(this)

  this._torrent = torrent
  this._destroyed = false

  this.name = file.name
  this.path = file.path
  this.length = file.length
  this.offset = file.offset

  this.done = false

  var start = file.offset
  var end = start + file.length - 1

  this._startPiece = start / this._torrent.pieceLength | 0
  this._endPiece = end / this._torrent.pieceLength | 0

  if (this.length === 0) {
    this.done = true
    this.emit('done')
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file_stream"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>file_stream (file, opts)](#apidoc.element.webtorrent.file_stream)
- description and source-code
```javascript
function FileStream(file, opts) {
  stream.Readable.call(this, opts)

  this.destroyed = false
  this._torrent = file._torrent

  var start = (opts && opts.start) || 0
  var end = (opts && opts.end && opts.end < file.length)
    ? opts.end
    : file.length - 1

  var pieceLength = file._torrent.pieceLength

  this._startPiece = (start + file.offset) / pieceLength | 0
  this._endPiece = (end + file.offset) / pieceLength | 0

  this._piece = this._startPiece
  this._offset = (start + file.offset) - (this._startPiece * pieceLength)

  this._missing = end - start + 1
  this._reading = false
  this._notifying = false
  this._criticalLength = Math.min((1024 * 1024 / pieceLength) | 0, 2)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.rarity_map"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>rarity_map (torrent)](#apidoc.element.webtorrent.rarity_map)
- description and source-code
```javascript
function RarityMap(torrent) {
  var self = this

  self._torrent = torrent
  self._numPieces = torrent.pieces.length
  self._pieces = []

  self._onWire = function (wire) {
    self.recalculate()
    self._initWire(wire)
  }
  self._onWireHave = function (index) {
    self._pieces[index] += 1
  }
  self._onWireBitfield = function () {
    self.recalculate()
  }

  self._torrent.wires.forEach(function (wire) {
    self._initWire(wire)
  })
  self._torrent.on('wire', self._onWire)
  self.recalculate()
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

#### <a name="apidoc.element.webtorrent.tcp_pool"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>tcp_pool (client)](#apidoc.element.webtorrent.tcp_pool)
- description and source-code
```javascript
function TCPPool(client) {
  var self = this
  debug('create tcp pool (port %s)', client.torrentPort)

  self.server = net.createServer()
  self._client = client

  // Temporarily store incoming connections so they can be destroyed if the server is
  // closed before the connection is passed off to a Torrent.
  self._pendingConns = []

  self._onConnectionBound = function (conn) {
    self._onConnection(conn)
  }

  self._onListening = function () {
    self._client._onListening()
  }

  self._onError = function (err) {
    self._client._destroy(err)
  }

  self.server.on('connection', self._onConnectionBound)
  self.server.on('listening', self._onListening)
  self.server.on('error', self._onError)

  self.server.listen(client.torrentPort)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.torrent"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>torrent (torrentId, client, opts)](#apidoc.element.webtorrent.torrent)
- description and source-code
```javascript
function Torrent(torrentId, client, opts) {
  EventEmitter.call(this)

  this._debugId = 'unknown infohash'
  this.client = client

  this.announce = opts.announce
  this.urlList = opts.urlList

  this.path = opts.path
  this._store = opts.store || FSChunkStore
  this._getAnnounceOpts = opts.getAnnounceOpts

  this.strategy = opts.strategy || 'sequential'

  this.maxWebConns = opts.maxWebConns || 4

  this._rechokeNumSlots = (opts.uploads === false || opts.uploads === 0)
    ? 0
    : (+opts.uploads || 10)
  this._rechokeOptimisticWire = null
  this._rechokeOptimisticTime = 0
  this._rechokeIntervalId = null

  this.ready = false
  this.destroyed = false
  this.paused = false
  this.done = false

  this.metadata = null
  this.store = null
  this.files = []
  this.pieces = []

  this._amInterested = false
  this._selections = []
  this._critical = []

  this.wires = [] // open wires (added *after* handshake)

  this._queue = [] // queue of outgoing tcp peers to connect to
  this._peers = {} // connected peers (addr/peerId -> Peer)
  this._peersLength = 0 // number of elements in 'this._peers' (cache, for perf)

  // stats
  this.received = 0
  this.uploaded = 0
  this._downloadSpeed = speedometer()
  this._uploadSpeed = speedometer()

  // for cleanup
  this._servers = []
  this._xsRequests = []

  // TODO: remove this and expose a hook instead
  // optimization: don't recheck every file if it hasn't changed
  this._fileModtimes = opts.fileModtimes

  if (torrentId !== null) this._onTorrentId(torrentId)

  this._debug('new torrent')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.webconn"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>webconn (url, torrent)](#apidoc.element.webtorrent.webconn)
- description and source-code
```javascript
function WebConn(url, torrent) {
  Wire.call(this)

  this.url = url
  this.webPeerId = sha1.sync(url)
  this._torrent = torrent

  this._init()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webtorrent.file"></a>[module webtorrent.file](#apidoc.module.webtorrent.file)

#### <a name="apidoc.element.webtorrent.file.file"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>file (torrent, file)](#apidoc.element.webtorrent.file.file)
- description and source-code
```javascript
function File(torrent, file) {
  EventEmitter.call(this)

  this._torrent = torrent
  this._destroyed = false

  this.name = file.name
  this.path = file.path
  this.length = file.length
  this.offset = file.offset

  this.done = false

  var start = file.offset
  var end = start + file.length - 1

  this._startPiece = start / this._torrent.pieceLength | 0
  this._endPiece = end / this._torrent.pieceLength | 0

  if (this.length === 0) {
    this.done = true
    this.emit('done')
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file.super_"></a>[function <span class="apidocSignatureSpan">webtorrent.file.</span>super_ ()](#apidoc.element.webtorrent.file.super_)
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



# <a name="apidoc.module.webtorrent.file.prototype"></a>[module webtorrent.file.prototype](#apidoc.module.webtorrent.file.prototype)

#### <a name="apidoc.element.webtorrent.file.prototype._destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>_destroy ()](#apidoc.element.webtorrent.file.prototype._destroy)
- description and source-code
```javascript
_destroy = function () {
  this._destroyed = true
  this._torrent = null
}
```
- example usage
```shell
...
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
...
```

#### <a name="apidoc.element.webtorrent.file.prototype._getMimeType"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>_getMimeType ()](#apidoc.element.webtorrent.file.prototype._getMimeType)
- description and source-code
```javascript
_getMimeType = function () {
  return render.mime[path.extname(this.name).toLowerCase()]
}
```
- example usage
```shell
...

File.prototype.getBuffer = function (cb) {
  streamToBuffer(this.createReadStream(), this.length, cb)
}

File.prototype.getBlob = function (cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  streamToBlob(this.createReadStream(), this._getMimeType(), cb)
}

File.prototype.getBlobURL = function (cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  streamToBlobURL(this.createReadStream(), this._getMimeType(), cb)
}
...
```

#### <a name="apidoc.element.webtorrent.file.prototype.appendTo"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>appendTo (elem, opts, cb)](#apidoc.element.webtorrent.file.prototype.appendTo)
- description and source-code
```javascript
appendTo = function (elem, opts, cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  render.append(this, elem, opts, cb)
}
```
- example usage
```shell
...
client.add(magnetURI, function (torrent) {
  // Got torrent metadata!
  console.log('Client is downloading:', torrent.infoHash)

  torrent.files.forEach(function (file) {
    // Display the file by appending it to the DOM. Supports video, audio, images, and
    // more. Specify a container element (CSS selector or reference to DOM node).
    file.appendTo('body')
  })
})
'''

##### Seeding a file is simple, too:

'''js
...
```

#### <a name="apidoc.element.webtorrent.file.prototype.createReadStream"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>createReadStream (opts)](#apidoc.element.webtorrent.file.prototype.createReadStream)
- description and source-code
```javascript
createReadStream = function (opts) {
  var self = this
  if (this.length === 0) {
    var empty = new stream.PassThrough()
    process.nextTick(function () {
      empty.end()
    })
    return empty
  }

  var fileStream = new FileStream(self, opts)
  self._torrent.select(fileStream._startPiece, fileStream._endPiece, true, function () {
    fileStream._notify()
  })
  eos(fileStream, function () {
    if (self._destroyed) return
    if (!self._torrent.destroyed) {
      self._torrent.deselect(fileStream._startPiece, fileStream._endPiece, true)
    }
  })
  return fileStream
}
```
- example usage
```shell
...
      self._torrent.deselect(fileStream._startPiece, fileStream._endPiece, true)
    }
  })
  return fileStream
}

File.prototype.getBuffer = function (cb) {
  streamToBuffer(this.createReadStream(), this.length, cb)
}

File.prototype.getBlob = function (cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  streamToBlob(this.createReadStream(), this._getMimeType(), cb)
}
...
```

#### <a name="apidoc.element.webtorrent.file.prototype.deselect"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>deselect ()](#apidoc.element.webtorrent.file.prototype.deselect)
- description and source-code
```javascript
deselect = function () {
  if (this.length === 0) return
  this._torrent.deselect(this._startPiece, this._endPiece, false)
}
```
- example usage
```shell
...
}

FileStream.prototype._destroy = function (err, onclose) {
  if (this.destroyed) return
  this.destroyed = true

  if (!this._torrent.destroyed) {
    this._torrent.deselect(this._startPiece, this._endPiece, true)
  }

  if (err) this.emit('error', err)
  this.emit('close')
  if (onclose) onclose()
}
...
```

#### <a name="apidoc.element.webtorrent.file.prototype.getBlob"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBlob (cb)](#apidoc.element.webtorrent.file.prototype.getBlob)
- description and source-code
```javascript
getBlob = function (cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  streamToBlob(this.createReadStream(), this._getMimeType(), cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file.prototype.getBlobURL"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBlobURL (cb)](#apidoc.element.webtorrent.file.prototype.getBlobURL)
- description and source-code
```javascript
getBlobURL = function (cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  streamToBlobURL(this.createReadStream(), this._getMimeType(), cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file.prototype.getBuffer"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>getBuffer (cb)](#apidoc.element.webtorrent.file.prototype.getBuffer)
- description and source-code
```javascript
getBuffer = function (cb) {
  streamToBuffer(this.createReadStream(), this.length, cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file.prototype.renderTo"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>renderTo (elem, opts, cb)](#apidoc.element.webtorrent.file.prototype.renderTo)
- description and source-code
```javascript
renderTo = function (elem, opts, cb) {
  if (typeof window === 'undefined') throw new Error('browser-only method')
  render.render(this, elem, opts, cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file.prototype.select"></a>[function <span class="apidocSignatureSpan">webtorrent.file.prototype.</span>select (priority)](#apidoc.element.webtorrent.file.prototype.select)
- description and source-code
```javascript
select = function (priority) {
  if (this.length === 0) return
  this._torrent.select(this._startPiece, this._endPiece, priority)
}
```
- example usage
```shell
...
    }
    return downloaded
  }
})

File.prototype.select = function (priority) {
  if (this.length === 0) return
  this._torrent.select(this._startPiece, this._endPiece, priority)
}

File.prototype.deselect = function () {
  if (this.length === 0) return
  this._torrent.deselect(this._startPiece, this._endPiece, false)
}
...
```



# <a name="apidoc.module.webtorrent.file_stream"></a>[module webtorrent.file_stream](#apidoc.module.webtorrent.file_stream)

#### <a name="apidoc.element.webtorrent.file_stream.file_stream"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>file_stream (file, opts)](#apidoc.element.webtorrent.file_stream.file_stream)
- description and source-code
```javascript
function FileStream(file, opts) {
  stream.Readable.call(this, opts)

  this.destroyed = false
  this._torrent = file._torrent

  var start = (opts && opts.start) || 0
  var end = (opts && opts.end && opts.end < file.length)
    ? opts.end
    : file.length - 1

  var pieceLength = file._torrent.pieceLength

  this._startPiece = (start + file.offset) / pieceLength | 0
  this._endPiece = (end + file.offset) / pieceLength | 0

  this._piece = this._startPiece
  this._offset = (start + file.offset) - (this._startPiece * pieceLength)

  this._missing = end - start + 1
  this._reading = false
  this._notifying = false
  this._criticalLength = Math.min((1024 * 1024 / pieceLength) | 0, 2)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file_stream.super_"></a>[function <span class="apidocSignatureSpan">webtorrent.file_stream.</span>super_ (options)](#apidoc.element.webtorrent.file_stream.super_)
- description and source-code
```javascript
function Readable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  if (!(this instanceof Readable)) return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function') this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webtorrent.file_stream.prototype"></a>[module webtorrent.file_stream.prototype](#apidoc.module.webtorrent.file_stream.prototype)

#### <a name="apidoc.element.webtorrent.file_stream.prototype._destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_destroy (err, onclose)](#apidoc.element.webtorrent.file_stream.prototype._destroy)
- description and source-code
```javascript
_destroy = function (err, onclose) {
  if (this.destroyed) return
  this.destroyed = true

  if (!this._torrent.destroyed) {
    this._torrent.deselect(this._startPiece, this._endPiece, true)
  }

  if (err) this.emit('error', err)
  this.emit('close')
  if (onclose) onclose()
}
```
- example usage
```shell
...
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
...
```

#### <a name="apidoc.element.webtorrent.file_stream.prototype._notify"></a>[function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_notify ()](#apidoc.element.webtorrent.file_stream.prototype._notify)
- description and source-code
```javascript
_notify = function () {
  var self = this

  if (!self._reading || self._missing === 0) return
  if (!self._torrent.bitfield.get(self._piece)) {
    return self._torrent.critical(self._piece, self._piece + self._criticalLength)
  }

  if (self._notifying) return
  self._notifying = true

  var p = self._piece
  self._torrent.store.get(p, function (err, buffer) {
    self._notifying = false
    if (self.destroyed) return
    if (err) return self._destroy(err)
    debug('read %s (length %s) (err %s)', p, buffer.length, err && err.message)

    if (self._offset) {
      buffer = buffer.slice(self._offset)
      self._offset = 0
    }

    if (self._missing < buffer.length) {
      buffer = buffer.slice(0, self._missing)
    }
    self._missing -= buffer.length

    debug('pushing buffer of length %s', buffer.length)
    self._reading = false
    self.push(buffer)

    if (self._missing === 0) self.push(null)
  })
  self._piece += 1
}
```
- example usage
```shell
...
this._notifying = false
this._criticalLength = Math.min((1024 * 1024 / pieceLength) | 0, 2)
}

FileStream.prototype._read = function () {
if (this._reading) return
this._reading = true
this._notify()
}

FileStream.prototype._notify = function () {
var self = this

if (!self._reading || self._missing === 0) return
if (!self._torrent.bitfield.get(self._piece)) {
...
```

#### <a name="apidoc.element.webtorrent.file_stream.prototype._read"></a>[function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>_read ()](#apidoc.element.webtorrent.file_stream.prototype._read)
- description and source-code
```javascript
_read = function () {
  if (this._reading) return
  this._reading = true
  this._notify()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.file_stream.prototype.destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.file_stream.prototype.</span>destroy (onclose)](#apidoc.element.webtorrent.file_stream.prototype.destroy)
- description and source-code
```javascript
destroy = function (onclose) {
  this._destroy(null, onclose)
}
```
- example usage
```shell
...
this._remove(torrentId, cb)
}

WebTorrent.prototype._remove = function (torrentId, cb) {
var torrent = this.get(torrentId)
if (!torrent) return
this.torrents.splice(this.torrents.indexOf(torrent), 1)
torrent.destroy(cb)
}

WebTorrent.prototype.address = function () {
if (!this.listening) return null
return this._tcpPool
  ? this._tcpPool.server.address()
  : { address: '0.0.0.0', family: 'IPv4', port: 0 }
...
```



# <a name="apidoc.module.webtorrent.peer"></a>[module webtorrent.peer](#apidoc.module.webtorrent.peer)

#### <a name="apidoc.element.webtorrent.peer.createTCPIncomingPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.peer.</span>createTCPIncomingPeer (conn)](#apidoc.element.webtorrent.peer.createTCPIncomingPeer)
- description and source-code
```javascript
createTCPIncomingPeer = function (conn) {
  var addr = conn.remoteAddress + ':' + conn.remotePort
  var peer = new Peer(addr, 'tcpIncoming')
  peer.conn = conn
  peer.addr = addr

  peer.onConnect()

  return peer
}
```
- example usage
```shell
...
  conn.destroy()
  return
}

self._pendingConns.push(conn)
conn.once('close', cleanupPending)

var peer = Peer.createTCPIncomingPeer(conn)

var wire = peer.wire
wire.once('handshake', onHandshake)

function onHandshake (infoHash, peerId) {
  cleanupPending()
...
```

#### <a name="apidoc.element.webtorrent.peer.createTCPOutgoingPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.peer.</span>createTCPOutgoingPeer (addr, swarm)](#apidoc.element.webtorrent.peer.createTCPOutgoingPeer)
- description and source-code
```javascript
createTCPOutgoingPeer = function (addr, swarm) {
  var peer = new Peer(addr, 'tcpOutgoing')
  peer.addr = addr
  peer.swarm = swarm

  return peer
}
```
- example usage
```shell
...
}

self._debug('add peer %s', id)

var newPeer
if (typeof peer === 'string') {
  // 'peer' is an addr ("ip:port" string)
  newPeer = Peer.createTCPOutgoingPeer(peer, self)
} else {
  // 'peer' is a WebRTC connection (simple-peer)
  newPeer = Peer.createWebRTCPeer(peer, self)
}

self._peers[newPeer.id] = newPeer
self._peersLength += 1
...
```

#### <a name="apidoc.element.webtorrent.peer.createWebRTCPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.peer.</span>createWebRTCPeer (conn, swarm)](#apidoc.element.webtorrent.peer.createWebRTCPeer)
- description and source-code
```javascript
createWebRTCPeer = function (conn, swarm) {
  var peer = new Peer(conn.id, 'webrtc')
  peer.conn = conn
  peer.swarm = swarm

  if (peer.conn.connected) {
    peer.onConnect()
  } else {
    peer.conn.once('connect', function () { peer.onConnect() })
    peer.conn.once('error', function (err) { peer.destroy(err) })
    peer.startConnectTimeout()
  }

  return peer
}
```
- example usage
```shell
...

var newPeer
if (typeof peer === 'string') {
  // 'peer' is an addr ("ip:port" string)
  newPeer = Peer.createTCPOutgoingPeer(peer, self)
} else {
  // 'peer' is a WebRTC connection (simple-peer)
  newPeer = Peer.createWebRTCPeer(peer, self)
}

self._peers[newPeer.id] = newPeer
self._peersLength += 1

if (typeof peer === 'string') {
  // 'peer' is an addr ("ip:port" string)
...
```

#### <a name="apidoc.element.webtorrent.peer.createWebSeedPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.peer.</span>createWebSeedPeer (url, swarm)](#apidoc.element.webtorrent.peer.createWebSeedPeer)
- description and source-code
```javascript
createWebSeedPeer = function (url, swarm) {
  var peer = new Peer(url, 'webSeed')
  peer.swarm = swarm
  peer.conn = new WebConn(url, swarm)

  peer.onConnect()

  return peer
}
```
- example usage
```shell
...
    this.emit('warning', new Error('ignoring duplicate web seed: ' + url))
    this.emit('invalidPeer', url)
    return
  }

  this._debug('add web seed %s', url)

  var newPeer = Peer.createWebSeedPeer(url, this)
  this._peers[newPeer.id] = newPeer
  this._peersLength += 1

  this.emit('peer', url)
}

/**
...
```



# <a name="apidoc.module.webtorrent.rarity_map"></a>[module webtorrent.rarity_map](#apidoc.module.webtorrent.rarity_map)

#### <a name="apidoc.element.webtorrent.rarity_map.rarity_map"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>rarity_map (torrent)](#apidoc.element.webtorrent.rarity_map.rarity_map)
- description and source-code
```javascript
function RarityMap(torrent) {
  var self = this

  self._torrent = torrent
  self._numPieces = torrent.pieces.length
  self._pieces = []

  self._onWire = function (wire) {
    self.recalculate()
    self._initWire(wire)
  }
  self._onWireHave = function (index) {
    self._pieces[index] += 1
  }
  self._onWireBitfield = function () {
    self.recalculate()
  }

  self._torrent.wires.forEach(function (wire) {
    self._initWire(wire)
  })
  self._torrent.on('wire', self._onWire)
  self.recalculate()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webtorrent.rarity_map.prototype"></a>[module webtorrent.rarity_map.prototype](#apidoc.module.webtorrent.rarity_map.prototype)

#### <a name="apidoc.element.webtorrent.rarity_map.prototype._cleanupWireEvents"></a>[function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>_cleanupWireEvents (wire)](#apidoc.element.webtorrent.rarity_map.prototype._cleanupWireEvents)
- description and source-code
```javascript
_cleanupWireEvents = function (wire) {
  wire.removeListener('have', this._onWireHave)
  wire.removeListener('bitfield', this._onWireBitfield)
  if (wire._onClose) wire.removeListener('close', wire._onClose)
  wire._onClose = null
}
```
- example usage
```shell
...
}
}

RarityMap.prototype.destroy = function () {
var self = this
self._torrent.removeListener('wire', self._onWire)
self._torrent.wires.forEach(function (wire) {
  self._cleanupWireEvents(wire)
})
self._torrent = null
self._pieces = null

self._onWire = null
self._onWireHave = null
self._onWireBitfield = null
...
```

#### <a name="apidoc.element.webtorrent.rarity_map.prototype._initWire"></a>[function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>_initWire (wire)](#apidoc.element.webtorrent.rarity_map.prototype._initWire)
- description and source-code
```javascript
_initWire = function (wire) {
  var self = this

  wire._onClose = function () {
    self._cleanupWireEvents(wire)
    for (var i = 0; i < this._numPieces; ++i) {
      self._pieces[i] -= wire.peerPieces.get(i)
    }
  }

  wire.on('have', self._onWireHave)
  wire.on('bitfield', self._onWireBitfield)
  wire.once('close', wire._onClose)
}
```
- example usage
```shell
...

self._torrent = torrent
self._numPieces = torrent.pieces.length
self._pieces = []

self._onWire = function (wire) {
  self.recalculate()
  self._initWire(wire)
}
self._onWireHave = function (index) {
  self._pieces[index] += 1
}
self._onWireBitfield = function () {
  self.recalculate()
}
...
```

#### <a name="apidoc.element.webtorrent.rarity_map.prototype.destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>destroy ()](#apidoc.element.webtorrent.rarity_map.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  var self = this
  self._torrent.removeListener('wire', self._onWire)
  self._torrent.wires.forEach(function (wire) {
    self._cleanupWireEvents(wire)
  })
  self._torrent = null
  self._pieces = null

  self._onWire = null
  self._onWireHave = null
  self._onWireBitfield = null
}
```
- example usage
```shell
...
this._remove(torrentId, cb)
}

WebTorrent.prototype._remove = function (torrentId, cb) {
var torrent = this.get(torrentId)
if (!torrent) return
this.torrents.splice(this.torrents.indexOf(torrent), 1)
torrent.destroy(cb)
}

WebTorrent.prototype.address = function () {
if (!this.listening) return null
return this._tcpPool
  ? this._tcpPool.server.address()
  : { address: '0.0.0.0', family: 'IPv4', port: 0 }
...
```

#### <a name="apidoc.element.webtorrent.rarity_map.prototype.getRarestPiece"></a>[function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>getRarestPiece (pieceFilterFunc)](#apidoc.element.webtorrent.rarity_map.prototype.getRarestPiece)
- description and source-code
```javascript
getRarestPiece = function (pieceFilterFunc) {
  if (!pieceFilterFunc) pieceFilterFunc = trueFn

  var candidates = []
  var min = Infinity

  for (var i = 0; i < this._numPieces; ++i) {
    if (!pieceFilterFunc(i)) continue

    var availability = this._pieces[i]
    if (availability === min) {
      candidates.push(i)
    } else if (availability < min) {
      candidates = [ i ]
      min = availability
    }
  }

  if (candidates.length > 0) {
    // if there are multiple pieces with the same availability, choose one randomly
    return candidates[Math.random() * candidates.length | 0]
  } else {
    return -1
  }
}
```
- example usage
```shell
...
  var end = next.to
  var len = end - start + 1
  var tried = {}
  var tries = 0
  var filter = genPieceFilterFunc(start, end, tried)

  while (tries < len) {
    piece = self._rarityMap.getRarestPiece(filter)
    if (piece < 0) break
    if (self._request(wire, piece, false)) return
    tried[piece] = true
    tries += 1
  }
} else {
  for (piece = next.to; piece >= next.from + next.offset; --piece) {
...
```

#### <a name="apidoc.element.webtorrent.rarity_map.prototype.recalculate"></a>[function <span class="apidocSignatureSpan">webtorrent.rarity_map.prototype.</span>recalculate ()](#apidoc.element.webtorrent.rarity_map.prototype.recalculate)
- description and source-code
```javascript
recalculate = function () {
  var i
  for (i = 0; i < this._numPieces; ++i) {
    this._pieces[i] = 0
  }

  var numWires = this._torrent.wires.length
  for (i = 0; i < numWires; ++i) {
    var wire = this._torrent.wires[i]
    for (var j = 0; j < this._numPieces; ++j) {
      this._pieces[j] += wire.peerPieces.get(j)
    }
  }
}
```
- example usage
```shell
...
var self = this

self._torrent = torrent
self._numPieces = torrent.pieces.length
self._pieces = []

self._onWire = function (wire) {
  self.recalculate()
  self._initWire(wire)
}
self._onWireHave = function (index) {
  self._pieces[index] += 1
}
self._onWireBitfield = function () {
  self.recalculate()
...
```



# <a name="apidoc.module.webtorrent.tcp_pool"></a>[module webtorrent.tcp_pool](#apidoc.module.webtorrent.tcp_pool)

#### <a name="apidoc.element.webtorrent.tcp_pool.tcp_pool"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>tcp_pool (client)](#apidoc.element.webtorrent.tcp_pool.tcp_pool)
- description and source-code
```javascript
function TCPPool(client) {
  var self = this
  debug('create tcp pool (port %s)', client.torrentPort)

  self.server = net.createServer()
  self._client = client

  // Temporarily store incoming connections so they can be destroyed if the server is
  // closed before the connection is passed off to a Torrent.
  self._pendingConns = []

  self._onConnectionBound = function (conn) {
    self._onConnection(conn)
  }

  self._onListening = function () {
    self._client._onListening()
  }

  self._onError = function (err) {
    self._client._destroy(err)
  }

  self.server.on('connection', self._onConnectionBound)
  self.server.on('listening', self._onListening)
  self.server.on('error', self._onError)

  self.server.listen(client.torrentPort)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webtorrent.tcp_pool.prototype"></a>[module webtorrent.tcp_pool.prototype](#apidoc.module.webtorrent.tcp_pool.prototype)

#### <a name="apidoc.element.webtorrent.tcp_pool.prototype._onConnection"></a>[function <span class="apidocSignatureSpan">webtorrent.tcp_pool.prototype.</span>_onConnection (conn)](#apidoc.element.webtorrent.tcp_pool.prototype._onConnection)
- description and source-code
```javascript
_onConnection = function (conn) {
  var self = this

  // If the connection has already been closed before the 'connect' event is fired,
  // then 'remoteAddress' will not be available, and we can't use this connection.
  // - Node.js issue: https://github.com/nodejs/node-v0.x-archive/issues/7566
  // - WebTorrent issue: https://github.com/feross/webtorrent/issues/398
  if (!conn.remoteAddress) {
    conn.on('error', noop)
    conn.destroy()
    return
  }

  self._pendingConns.push(conn)
  conn.once('close', cleanupPending)

  var peer = Peer.createTCPIncomingPeer(conn)

  var wire = peer.wire
  wire.once('handshake', onHandshake)

  function onHandshake (infoHash, peerId) {
    cleanupPending()

    var torrent = self._client.get(infoHash)
    if (torrent) {
      peer.swarm = torrent
      torrent._addIncomingPeer(peer)
      peer.onHandshake(infoHash, peerId)
    } else {
      var err = new Error(
        'Unexpected info hash ' + infoHash + ' from incoming peer ' + peer.id
      )
      peer.destroy(err)
    }
  }

  function cleanupPending () {
    conn.removeListener('close', cleanupPending)
    wire.removeListener('handshake', onHandshake)
    if (self._pendingConns) {
      arrayRemove(self._pendingConns, self._pendingConns.indexOf(conn))
    }
  }
}
```
- example usage
```shell
...
self._client = client

// Temporarily store incoming connections so they can be destroyed if the server is
// closed before the connection is passed off to a Torrent.
self._pendingConns = []

self._onConnectionBound = function (conn) {
  self._onConnection(conn)
}

self._onListening = function () {
  self._client._onListening()
}

self._onError = function (err) {
...
```

#### <a name="apidoc.element.webtorrent.tcp_pool.prototype.destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.tcp_pool.prototype.</span>destroy (cb)](#apidoc.element.webtorrent.tcp_pool.prototype.destroy)
- description and source-code
```javascript
destroy = function (cb) {
  var self = this
  debug('destroy tcp pool')

  self.server.removeListener('connection', self._onConnectionBound)
  self.server.removeListener('listening', self._onListening)
  self.server.removeListener('error', self._onError)

  // Destroy all open connection objects so server can close gracefully without waiting
  // for connection timeout or remote peer to disconnect.
  self._pendingConns.forEach(function (conn) {
    conn.on('error', noop)
    conn.destroy()
  })

  try {
    self.server.close(cb)
  } catch (err) {
    if (cb) process.nextTick(cb)
  }

  self.server = null
  self._client = null
  self._pendingConns = null
}
```
- example usage
```shell
...
this._remove(torrentId, cb)
}

WebTorrent.prototype._remove = function (torrentId, cb) {
var torrent = this.get(torrentId)
if (!torrent) return
this.torrents.splice(this.torrents.indexOf(torrent), 1)
torrent.destroy(cb)
}

WebTorrent.prototype.address = function () {
if (!this.listening) return null
return this._tcpPool
  ? this._tcpPool.server.address()
  : { address: '0.0.0.0', family: 'IPv4', port: 0 }
...
```



# <a name="apidoc.module.webtorrent.torrent"></a>[module webtorrent.torrent](#apidoc.module.webtorrent.torrent)

#### <a name="apidoc.element.webtorrent.torrent.torrent"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>torrent (torrentId, client, opts)](#apidoc.element.webtorrent.torrent.torrent)
- description and source-code
```javascript
function Torrent(torrentId, client, opts) {
  EventEmitter.call(this)

  this._debugId = 'unknown infohash'
  this.client = client

  this.announce = opts.announce
  this.urlList = opts.urlList

  this.path = opts.path
  this._store = opts.store || FSChunkStore
  this._getAnnounceOpts = opts.getAnnounceOpts

  this.strategy = opts.strategy || 'sequential'

  this.maxWebConns = opts.maxWebConns || 4

  this._rechokeNumSlots = (opts.uploads === false || opts.uploads === 0)
    ? 0
    : (+opts.uploads || 10)
  this._rechokeOptimisticWire = null
  this._rechokeOptimisticTime = 0
  this._rechokeIntervalId = null

  this.ready = false
  this.destroyed = false
  this.paused = false
  this.done = false

  this.metadata = null
  this.store = null
  this.files = []
  this.pieces = []

  this._amInterested = false
  this._selections = []
  this._critical = []

  this.wires = [] // open wires (added *after* handshake)

  this._queue = [] // queue of outgoing tcp peers to connect to
  this._peers = {} // connected peers (addr/peerId -> Peer)
  this._peersLength = 0 // number of elements in 'this._peers' (cache, for perf)

  // stats
  this.received = 0
  this.uploaded = 0
  this._downloadSpeed = speedometer()
  this._uploadSpeed = speedometer()

  // for cleanup
  this._servers = []
  this._xsRequests = []

  // TODO: remove this and expose a hook instead
  // optimization: don't recheck every file if it hasn't changed
  this._fileModtimes = opts.fileModtimes

  if (torrentId !== null) this._onTorrentId(torrentId)

  this._debug('new torrent')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.torrent.super_"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.</span>super_ ()](#apidoc.element.webtorrent.torrent.super_)
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



# <a name="apidoc.module.webtorrent.torrent.prototype"></a>[module webtorrent.torrent.prototype](#apidoc.module.webtorrent.torrent.prototype)

#### <a name="apidoc.element.webtorrent.torrent.prototype._addIncomingPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_addIncomingPeer (peer)](#apidoc.element.webtorrent.torrent.prototype._addIncomingPeer)
- description and source-code
```javascript
_addIncomingPeer = function (peer) {
  var self = this
  if (self.destroyed) return peer.destroy(new Error('torrent is destroyed'))
  if (self.paused) return peer.destroy(new Error('torrent is paused'))

  this._debug('add incoming peer %s', peer.id)

  self._peers[peer.id] = peer
  self._peersLength += 1
}
```
- example usage
```shell
...

  function onHandshake (infoHash, peerId) {
cleanupPending()

var torrent = self._client.get(infoHash)
if (torrent) {
  peer.swarm = torrent
  torrent._addIncomingPeer(peer)
  peer.onHandshake(infoHash, peerId)
} else {
  var err = new Error(
    'Unexpected info hash ' + infoHash + ' from incoming peer ' + peer.id
  )
  peer.destroy(err)
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._addPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_addPeer (peer)](#apidoc.element.webtorrent.torrent.prototype._addPeer)
- description and source-code
```javascript
_addPeer = function (peer) {
  var self = this
  if (self.destroyed) {
    if (typeof peer !== 'string') peer.destroy()
    return null
  }
  if (typeof peer === 'string' && !self._validAddr(peer)) {
    self._debug('ignoring peer: invalid %s', peer)
    return null
  }

  var id = (peer && peer.id) || peer
  if (self._peers[id]) {
    self._debug('ignoring peer: duplicate (%s)', id)
    if (typeof peer !== 'string') peer.destroy()
    return null
  }

  if (self.paused) {
    self._debug('ignoring peer: torrent is paused')
    if (typeof peer !== 'string') peer.destroy()
    return null
  }

  self._debug('add peer %s', id)

  var newPeer
  if (typeof peer === 'string') {
    // 'peer' is an addr ("ip:port" string)
    newPeer = Peer.createTCPOutgoingPeer(peer, self)
  } else {
    // 'peer' is a WebRTC connection (simple-peer)
    newPeer = Peer.createWebRTCPeer(peer, self)
  }

  self._peers[newPeer.id] = newPeer
  self._peersLength += 1

  if (typeof peer === 'string') {
    // 'peer' is an addr ("ip:port" string)
    self._queue.push(newPeer)
    self._drain()
  }

  return newPeer
}
```
- example usage
```shell
...
      self._debug('ignoring peer: blocked %s', peer)
      if (typeof peer !== 'string') peer.destroy()
      self.emit('blockedPeer', peer)
      return false
    }
  }

  var wasAdded = !!self._addPeer(peer)
  if (wasAdded) {
    self.emit('peer', peer)
  } else {
    self.emit('invalidPeer', peer)
  }
  return wasAdded
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._checkDone"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_checkDone ()](#apidoc.element.webtorrent.torrent.prototype._checkDone)
- description and source-code
```javascript
_checkDone = function () {
  var self = this
  if (self.destroyed) return

  // are any new files done?
  self.files.forEach(function (file) {
    if (file.done) return
    for (var i = file._startPiece; i <= file._endPiece; ++i) {
      if (!self.bitfield.get(i)) return
    }
    file.done = true
    file.emit('done')
    self._debug('file done: ' + file.name)
  })

  // is the torrent done? (if all current selections are satisfied, or there are
  // no selections, then torrent is done)
  var done = true
  for (var i = 0; i < self._selections.length; i++) {
    var selection = self._selections[i]
    for (var piece = selection.from; piece <= selection.to; piece++) {
      if (!self.bitfield.get(piece)) {
        done = false
        break
      }
    }
    if (!done) break
  }
  if (!self.done && done) {
    self.done = true
    self._debug('torrent done: ' + self.infoHash)
    self.emit('done')
  }
  self._gcSelections()

  return done
}
```
- example usage
```shell
...
if (self.destroyed) return
self._debug('on store')

self.ready = true
self.emit('ready')

// Files may start out done if the file was already in the store
self._checkDone()

// In case any selections were made before torrent was ready
self._updateSelections()
}

Torrent.prototype.destroy = function (cb) {
var self = this
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._debug"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_debug ()](#apidoc.element.webtorrent.torrent.prototype._debug)
- description and source-code
```javascript
_debug = function () {
  var args = [].slice.call(arguments)
  args[0] = '[' + this.client._debugId + '] [' + this._debugId + '] ' + args[0]
  debug.apply(null, args)
}
```
- example usage
```shell
...
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
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_destroy (err, cb)](#apidoc.element.webtorrent.torrent.prototype._destroy)
- description and source-code
```javascript
_destroy = function (err, cb) {
  var self = this
  if (self.destroyed) return
  self.destroyed = true
  self._debug('destroy')

  self.client._remove(self)

  clearInterval(self._rechokeIntervalId)

  self._xsRequests.forEach(function (req) {
    req.abort()
  })

  if (self._rarityMap) {
    self._rarityMap.destroy()
  }

  for (var id in self._peers) {
    self.removePeer(id)
  }

  self.files.forEach(function (file) {
    if (file instanceof File) file._destroy()
  })

  var tasks = self._servers.map(function (server) {
    return function (cb) {
      server.destroy(cb)
    }
  })

  if (self.discovery) {
    tasks.push(function (cb) {
      self.discovery.destroy(cb)
    })
  }

  if (self.store) {
    tasks.push(function (cb) {
      self.store.close(cb)
    })
  }

  parallel(tasks, cb)

  if (err) {
    // Torrent errors are emitted at 'torrent.on('error')'. If there are no 'error'
    // event handlers on the torrent instance, then the error will be emitted at
    // 'client.on('error')'. This prevents throwing an uncaught exception
    // (unhandled 'error' event), but it makes it impossible to distinguish client
    // errors versus torrent errors. Torrent errors are not fatal, and the client
    // is still usable afterwards. Therefore, always listen for errors in both
    // places ('client.on('error')' and 'torrent.on('error')').
    if (self.listenerCount('error') === 0) {
      self.client.emit('error', err)
    } else {
      self.emit('error', err)
    }
  }

  self.emit('close')

  self.client = null
  self.files = []
  self.discovery = null
  self.store = null
  self._rarityMap = null
  self._peers = null
  self._servers = null
  self._xsRequests = null
}
```
- example usage
```shell
...
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
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._drain"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_drain ()](#apidoc.element.webtorrent.torrent.prototype._drain)
- description and source-code
```javascript
_drain = function () {
  var self = this
  this._debug('_drain numConns %s maxConns %s', self._numConns, self.client.maxConns)
  if (typeof net.connect !== 'function' || self.destroyed || self.paused ||
      self._numConns >= self.client.maxConns) {
    return
  }
  this._debug('drain (%s queued, %s/%s peers)', self._numQueued, self.numPeers, self.client.maxConns)

  var peer = self._queue.shift()
  if (!peer) return // queue could be empty

  this._debug('tcp connect attempt to %s', peer.addr)

  var parts = addrToIPPort(peer.addr)
  var opts = {
    host: parts[0],
    port: parts[1]
  }

  var conn = peer.conn = net.connect(opts)

  conn.once('connect', function () { peer.onConnect() })
  conn.once('error', function (err) { peer.destroy(err) })
  peer.startConnectTimeout()

  // When connection closes, attempt reconnect after timeout (with exponential backoff)
  conn.on('close', function () {
    if (self.destroyed) return

    // TODO: If torrent is done, do not try to reconnect after a timeout

    if (peer.retries >= RECONNECT_WAIT.length) {
      self._debug(
        'conn %s closed: will not re-add (max %s attempts)',
        peer.addr, RECONNECT_WAIT.length
      )
      return
    }

    var ms = RECONNECT_WAIT[peer.retries]
    self._debug(
      'conn %s closed: will re-add to queue in %sms (attempt %s)',
      peer.addr, ms, peer.retries + 1
    )

    var reconnectTimeout = setTimeout(function reconnectTimeout () {
      var newPeer = self._addPeer(peer.addr)
      if (newPeer) newPeer.retries = peer.retries + 1
    }, ms)
    if (reconnectTimeout.unref) reconnectTimeout.unref()
  })
}
```
- example usage
```shell
...

self._peers[newPeer.id] = newPeer
self._peersLength += 1

if (typeof peer === 'string') {
  // 'peer' is an addr ("ip:port" string)
  self._queue.push(newPeer)
  self._drain()
}

return newPeer
}

Torrent.prototype.addWebSeed = function (url) {
if (this.destroyed) throw new Error('torrent is destroyed')
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._gcSelections"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_gcSelections ()](#apidoc.element.webtorrent.torrent.prototype._gcSelections)
- description and source-code
```javascript
_gcSelections = function () {
  var self = this

  for (var i = 0; i < self._selections.length; ++i) {
    var s = self._selections[i]
    var oldOffset = s.offset

    // check for newly downloaded pieces in selection
    while (self.bitfield.get(s.from + s.offset) && s.from + s.offset < s.to) {
      s.offset += 1
    }

    if (oldOffset !== s.offset) s.notify()
    if (s.to !== s.from + s.offset) continue
    if (!self.bitfield.get(s.from + s.offset)) continue

    self._selections.splice(i, 1) // remove fully downloaded selection
    i -= 1 // decrement i to offset splice

    s.notify()
    self._updateInterest()
  }

  if (!self._selections.length) self.emit('idle')
}
```
- example usage
```shell
...
* Called on selection changes.
*/
Torrent.prototype._updateSelections = function () {
 var self = this
 if (!self.ready || self.destroyed) return

 process.nextTick(function () {
   self._gcSelections()
 })
 self._updateInterest()
 self._update()
}

/**
* Garbage collect selections with respect to the store's current state.
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._getMetadataFromServer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_getMetadataFromServer ()](#apidoc.element.webtorrent.torrent.prototype._getMetadataFromServer)
- description and source-code
```javascript
_getMetadataFromServer = function () {
  var self = this
  var urls = Array.isArray(self.xs) ? self.xs : [ self.xs ]

  var tasks = urls.map(function (url) {
    return function (cb) {
      getMetadataFromURL(url, cb)
    }
  })
  parallel(tasks)

  function getMetadataFromURL (url, cb) {
    if (url.indexOf('http://') !== 0 && url.indexOf('https://') !== 0) {
      self.emit('warning', new Error('skipping non-http xs param: ' + url))
      return cb(null)
    }

    var opts = {
      url: url,
      method: 'GET',
      headers: {
        'user-agent': USER_AGENT
      }
    }
    var req
    try {
      req = get.concat(opts, onResponse)
    } catch (err) {
      self.emit('warning', new Error('skipping invalid url xs param: ' + url))
      return cb(null)
    }

    self._xsRequests.push(req)

    function onResponse (err, res, torrent) {
      if (self.destroyed) return cb(null)
      if (self.metadata) return cb(null)

      if (err) {
        self.emit('warning', new Error('http error from xs param: ' + url))
        return cb(null)
      }
      if (res.statusCode !== 200) {
        self.emit('warning', new Error('non-200 status code ' + res.statusCode + ' from xs param: ' + url))
        return cb(null)
      }

      var parsedTorrent
      try {
        parsedTorrent = parseTorrent(torrent)
      } catch (err) {}

      if (!parsedTorrent) {
        self.emit('warning', new Error('got invalid torrent file from xs param: ' + url))
        return cb(null)
      }

      if (parsedTorrent.infoHash !== self.infoHash) {
        self.emit('warning', new Error('got torrent file with incorrect info hash from xs param: ' + url))
        return cb(null)
      }

      self._onMetadata(parsedTorrent)
      cb(null)
    }
  }
}
```
- example usage
```shell
...
}

if (self.info) {
  // if full metadata was included in initial torrent id, use it immediately. Otherwise,
  // wait for torrent-discovery to find peers and ut_metadata to get the metadata.
  self._onMetadata(self)
} else if (self.xs) {
  self._getMetadataFromServer()
}
}

Torrent.prototype._getMetadataFromServer = function () {
var self = this
var urls = Array.isArray(self.xs) ? self.xs : [ self.xs ]
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._hotswap"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_hotswap (wire, index)](#apidoc.element.webtorrent.torrent.prototype._hotswap)
- description and source-code
```javascript
_hotswap = function (wire, index) {
  var self = this

  var speed = wire.downloadSpeed()
  if (speed < Piece.BLOCK_LENGTH) return false
  if (!self._reservations[index]) return false

  var r = self._reservations[index]
  if (!r) {
    return false
  }

  var minSpeed = Infinity
  var minWire

  var i
  for (i = 0; i < r.length; i++) {
    var otherWire = r[i]
    if (!otherWire || otherWire === wire) continue

    var otherSpeed = otherWire.downloadSpeed()
    if (otherSpeed >= SPEED_THRESHOLD) continue
    if (2 * otherSpeed > speed || otherSpeed > minSpeed) continue

    minWire = otherWire
    minSpeed = otherSpeed
  }

  if (!minWire) return false

  for (i = 0; i < r.length; i++) {
    if (r[i] === minWire) r[i] = null
  }

  for (i = 0; i < minWire.requests.length; i++) {
    var req = minWire.requests[i]
    if (req.piece !== index) continue

    self.pieces[index].cancel((req.offset / Piece.BLOCK_LENGTH) | 0)
  }

  self.emit('hotswap', minWire, wire, index)
  return true
}
```
- example usage
```shell
...

if (numRequests >= maxOutstandingRequests) return false
// var endGame = (wire.requests.length === 0 && self.store.numMissing < 30)

var piece = self.pieces[index]
var reservation = isWebSeed ? piece.reserveRemaining() : piece.reserve()

if (reservation === -1 && hotswap && self._hotswap(wire, index)) {
  reservation = isWebSeed ? piece.reserveRemaining() : piece.reserve()
}
if (reservation === -1) return false

var r = self._reservations[index]
if (!r) r = self._reservations[index] = []
var i = r.indexOf(null)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._markVerified"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_markVerified (index)](#apidoc.element.webtorrent.torrent.prototype._markVerified)
- description and source-code
```javascript
_markVerified = function (index) {
  this.pieces[index] = null
  this._reservations[index] = null
  this.bitfield.set(index, true)
}
```
- example usage
```shell
...
      return fileModtimes[index] === self._fileModtimes[index]
    }).every(function (x) {
      return x
    })

    if (unchanged) {
      for (var index = 0; index < self.pieces.length; index++) {
        self._markVerified(index)
      }
      self._onStore()
    } else {
      self._verifyPieces()
    }
  })
} else {
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onListening"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onListening ()](#apidoc.element.webtorrent.torrent.prototype._onListening)
- description and source-code
```javascript
_onListening = function () {
  var self = this
  if (self.discovery || self.destroyed) return

  var trackerOpts = self.client.tracker
  if (trackerOpts) {
    trackerOpts = extend(self.client.tracker, {
      getAnnounceOpts: function () {
        var opts = {
          uploaded: self.uploaded,
          downloaded: self.downloaded,
          left: Math.max(self.length - self.downloaded, 0)
        }
        if (self.client.tracker.getAnnounceOpts) {
          extendMutable(opts, self.client.tracker.getAnnounceOpts())
        }
        if (self._getAnnounceOpts) {
          // TODO: consider deprecating this, as it's redundant with the former case
          extendMutable(opts, self._getAnnounceOpts())
        }
        return opts
      }
    })
  }

  // begin discovering peers via DHT and trackers
  self.discovery = new Discovery({
    infoHash: self.infoHash,
    announce: self.announce,
    peerId: self.client.peerId,
    dht: !self.private && self.client.dht,
    tracker: trackerOpts,
    port: self.client.torrentPort,
    userAgent: USER_AGENT
  })

  self.discovery.on('error', onError)
  self.discovery.on('peer', onPeer)
  self.discovery.on('trackerAnnounce', onTrackerAnnounce)
  self.discovery.on('dhtAnnounce', onDHTAnnounce)
  self.discovery.on('warning', onWarning)

  function onError (err) {
    self._destroy(err)
  }

  function onPeer (peer) {
    // Don't create new outgoing TCP connections when torrent is done
    if (typeof peer === 'string' && self.done) return
    self.addPeer(peer)
  }

  function onTrackerAnnounce () {
    self.emit('trackerAnnounce')
    if (self.numPeers === 0) self.emit('noPeers', 'tracker')
  }

  function onDHTAnnounce () {
    self.emit('dhtAnnounce')
    if (self.numPeers === 0) self.emit('noPeers', 'dht')
  }

  function onWarning (err) {
    self.emit('warning', err)
  }

  if (self.info) {
    // if full metadata was included in initial torrent id, use it immediately. Otherwise,
    // wait for torrent-discovery to find peers and ut_metadata to get the metadata.
    self._onMetadata(self)
  } else if (self.xs) {
    self._getMetadataFromServer()
  }
}
```
- example usage
```shell
...
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
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onMetadata"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onMetadata (metadata)](#apidoc.element.webtorrent.torrent.prototype._onMetadata)
- description and source-code
```javascript
_onMetadata = function (metadata) {
  var self = this
  if (self.metadata || self.destroyed) return
  self._debug('got metadata')

  self._xsRequests.forEach(function (req) {
    req.abort()
  })
  self._xsRequests = []

  var parsedTorrent
  if (metadata && metadata.infoHash) {
    // 'metadata' is a parsed torrent (from parse-torrent module)
    parsedTorrent = metadata
  } else {
    try {
      parsedTorrent = parseTorrent(metadata)
    } catch (err) {
      return self._destroy(err)
    }
  }

  self._processParsedTorrent(parsedTorrent)
  self.metadata = self.torrentFile

  // add web seed urls (BEP19)
  if (self.client.enableWebSeeds) {
    self.urlList.forEach(function (url) {
      self.addWebSeed(url)
    })
  }

  // start off selecting the entire torrent with low priority
  if (self.pieces.length !== 0) {
    self.select(0, self.pieces.length - 1, false)
  }

  self._rarityMap = new RarityMap(self)

  self.store = new ImmediateChunkStore(
    new self._store(self.pieceLength, {
      torrent: {
        infoHash: self.infoHash
      },
      files: self.files.map(function (file) {
        return {
          path: path.join(self.path, file.path),
          length: file.length,
          offset: file.offset
        }
      }),
      length: self.length
    })
  )

  self.files = self.files.map(function (file) {
    return new File(self, file)
  })

  self._hashes = self.pieces

  self.pieces = self.pieces.map(function (hash, i) {
    var pieceLength = (i === self.pieces.length - 1)
      ? self.lastPieceLength
      : self.pieceLength
    return new Piece(pieceLength)
  })

  self._reservations = self.pieces.map(function () {
    return []
  })

  self.bitfield = new BitField(self.pieces.length)

  self.wires.forEach(function (wire) {
    // If we didn't have the metadata at the time ut_metadata was initialized for this
    // wire, we still want to make it available to the peer in case they request it.
    if (wire.ut_metadata) wire.ut_metadata.setMetadata(self.metadata)

    self._onWireWithMetadata(wire)
  })

  self._debug('verifying existing torrent data')
  if (self._fileModtimes && self._store === FSChunkStore) {
    // don't verify if the files haven't been modified since we last checked
    self.getFileModtimes(function (err, fileModtimes) {
      if (err) return self._destroy(err)

      var unchanged = self.files.map(function (_, index) {
        return fileModtimes[index] === self._fileModtimes[index]
      }).every(function (x) {
        return x
      })

      if (unchanged) {
        for (var index = 0; index < self.pieces.length; index++) {
          self._markVerified(index)
        }
        self._onStore()
      } else {
        self._verifyPieces()
      }
    })
  } else {
    self._verifyPieces()
  }

  self.emit('metadata')
}
```
- example usage
```shell
...
function onWarning (err) {
  self.emit('warning', err)
}

if (self.info) {
  // if full metadata was included in initial torrent id, use it immediately. Otherwise,
  // wait for torrent-discovery to find peers and ut_metadata to get the metadata.
  self._onMetadata(self)
} else if (self.xs) {
  self._getMetadataFromServer()
}
}

Torrent.prototype._getMetadataFromServer = function () {
var self = this
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onParsedTorrent"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onParsedTorrent (parsedTorrent)](#apidoc.element.webtorrent.torrent.prototype._onParsedTorrent)
- description and source-code
```javascript
_onParsedTorrent = function (parsedTorrent) {
  var self = this
  if (self.destroyed) return

  self._processParsedTorrent(parsedTorrent)

  if (!self.infoHash) {
    return self._destroy(new Error('Malformed torrent data: No info hash'))
  }

  if (!self.path) self.path = path.join(TMP, self.infoHash)

  self._rechokeIntervalId = setInterval(function () {
    self._rechoke()
  }, RECHOKE_INTERVAL)
  if (self._rechokeIntervalId.unref) self._rechokeIntervalId.unref()

  // Private 'infoHash' event allows client.add to check for duplicate torrents and
  // destroy them before the normal 'infoHash' event is emitted. Prevents user
  // applications from needing to deal with duplicate 'infoHash' events.
  self.emit('_infoHash', self.infoHash)
  if (self.destroyed) return

  self.emit('infoHash', self.infoHash)
  if (self.destroyed) return // user might destroy torrent in event handler

  if (self.client.listening) {
    self._onListening()
  } else {
    self.client.once('listening', function () {
      self._onListening()
    })
  }
}
```
- example usage
```shell
...
try { parsedTorrent = parseTorrent(torrentId) } catch (err) {}
if (parsedTorrent) {
  // Attempt to set infoHash property synchronously
  self.infoHash = parsedTorrent.infoHash
  self._debugId = parsedTorrent.infoHash.toString('hex').substring(0, 7)
  process.nextTick(function () {
    if (self.destroyed) return
    self._onParsedTorrent(parsedTorrent)
  })
} else {
  // If torrentId failed to parse, it could be in a form that requires an async
  // operation, i.e. http/https link, filesystem path, or Blob.
  parseTorrent.remote(torrentId, function (err, parsedTorrent) {
    if (self.destroyed) return
    if (err) return self._destroy(err)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onStore"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onStore ()](#apidoc.element.webtorrent.torrent.prototype._onStore)
- description and source-code
```javascript
_onStore = function () {
  var self = this
  if (self.destroyed) return
  self._debug('on store')

  self.ready = true
  self.emit('ready')

  // Files may start out done if the file was already in the store
  self._checkDone()

  // In case any selections were made before torrent was ready
  self._updateSelections()
}
```
- example usage
```shell
...
      return x
    })

    if (unchanged) {
      for (var index = 0; index < self.pieces.length; index++) {
        self._markVerified(index)
      }
      self._onStore()
    } else {
      self._verifyPieces()
    }
  })
} else {
  self._verifyPieces()
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onTorrentId"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onTorrentId (torrentId)](#apidoc.element.webtorrent.torrent.prototype._onTorrentId)
- description and source-code
```javascript
_onTorrentId = function (torrentId) {
  var self = this
  if (self.destroyed) return

  var parsedTorrent
  try { parsedTorrent = parseTorrent(torrentId) } catch (err) {}
  if (parsedTorrent) {
    // Attempt to set infoHash property synchronously
    self.infoHash = parsedTorrent.infoHash
    self._debugId = parsedTorrent.infoHash.toString('hex').substring(0, 7)
    process.nextTick(function () {
      if (self.destroyed) return
      self._onParsedTorrent(parsedTorrent)
    })
  } else {
    // If torrentId failed to parse, it could be in a form that requires an async
    // operation, i.e. http/https link, filesystem path, or Blob.
    parseTorrent.remote(torrentId, function (err, parsedTorrent) {
      if (self.destroyed) return
      if (err) return self._destroy(err)
      self._onParsedTorrent(parsedTorrent)
    })
  }
}
```
- example usage
```shell
...
      if (self.destroyed) return
      if (err) return torrent._destroy(err)

      var existingTorrent = self.get(torrentBuf)
      if (existingTorrent) {
        torrent._destroy(new Error('Cannot add duplicate torrent ' + existingTorrent.infoHash))
      } else {
        torrent._onTorrentId(torrentBuf)
      }
    })
  })
})

function onTorrent (torrent) {
  var tasks = [
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onWire"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onWire (wire, addr)](#apidoc.element.webtorrent.torrent.prototype._onWire)
- description and source-code
```javascript
_onWire = function (wire, addr) {
  var self = this
  self._debug('got wire %s (%s)', wire._debugId, addr || 'Unknown')

  wire.on('download', function (downloaded) {
    if (self.destroyed) return
    self.received += downloaded
    self._downloadSpeed(downloaded)
    self.client._downloadSpeed(downloaded)
    self.emit('download', downloaded)
    self.client.emit('download', downloaded)
  })

  wire.on('upload', function (uploaded) {
    if (self.destroyed) return
    self.uploaded += uploaded
    self._uploadSpeed(uploaded)
    self.client._uploadSpeed(uploaded)
    self.emit('upload', uploaded)
    self.client.emit('upload', uploaded)
  })

  self.wires.push(wire)

  if (addr) {
    // Sometimes RTCPeerConnection.getStats() doesn't return an ip:port for peers
    var parts = addrToIPPort(addr)
    wire.remoteAddress = parts[0]
    wire.remotePort = parts[1]
  }

  // When peer sends PORT message, add that DHT node to routing table
  if (self.client.dht && self.client.dht.listening) {
    wire.on('port', function (port) {
      if (self.destroyed || self.client.dht.destroyed) {
        return
      }
      if (!wire.remoteAddress) {
        return self._debug('ignoring PORT from peer with no address')
      }
      if (port === 0 || port > 65536) {
        return self._debug('ignoring invalid PORT from peer')
      }

      self._debug('port: %s (from %s)', port, addr)
      self.client.dht.addNode({ host: wire.remoteAddress, port: port })
    })
  }

  wire.on('timeout', function () {
    self._debug('wire timeout (%s)', addr)
    // TODO: this might be destroying wires too eagerly
    wire.destroy()
  })

  // Timeout for piece requests to this peer
  wire.setTimeout(PIECE_TIMEOUT, true)

  // Send KEEP-ALIVE (every 60s) so peers will not disconnect the wire
  wire.setKeepAlive(true)

  // use ut_metadata extension
  wire.use(utMetadata(self.metadata))

  wire.ut_metadata.on('warning', function (err) {
    self._debug('ut_metadata warning: %s', err.message)
  })

  if (!self.metadata) {
    wire.ut_metadata.on('metadata', function (metadata) {
      self._debug('got metadata via ut_metadata')
      self._onMetadata(metadata)
    })
    wire.ut_metadata.fetch()
  }

  // use ut_pex extension if the torrent is not flagged as private
  if (typeof utPex === 'function' && !self.private) {
    wire.use(utPex())

    wire.ut_pex.on('peer', function (peer) {
      // Only add potential new peers when we're not seeding
      if (self.done) return
      self._debug('ut_pex: got peer: %s (from %s)', peer, addr)
      self.addPeer(peer)
    })

    wire.ut_pex.on('dropped', function (peer) {
      // the remote peer believes a given peer has been dropped from the torrent swarm.
      // if we're not currently connected to it, then remove it from the queue.
      var peerObj = self._peers[peer]
      if (peerObj && !peerObj.connected) {
        self._debug('ut_pex: dropped peer: %s (from %s)', peer, addr)
        self.removePeer(peer)
      }
    })

    wire.once('close', function () {
      // Stop sending updates to remote peer
      wire.ut_pex.reset()
    })
  }

  // Hook to allow user-defined 'bittorrent-protocol' extensions
  // More info: https://github.com/feross/bittorrent-protocol#extension-api
  self.emit('wire', wire, addr)

  if (self.metadata) {
    process.nextTick(function () {
      // This allows wire.handshake() to be called (by Peer.onHandshake) before any
      // messages get sent on the wire
      self._onWireWithMetadata(wire)
    })
  }
}
```
- example usage
```shell
...

  self.retries = 0

  var addr = self.addr
  if (!addr && self.conn.remoteAddress) {
    addr = self.conn.remoteAddress + ':' + self.conn.remotePort
  }
  self.swarm._onWire(self.wire, addr)

  // swarm could be destroyed in user's 'wire' event handler
  if (!self.swarm || self.swarm.destroyed) return

  if (!self.sentHandshake) self.handshake()
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._onWireWithMetadata"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_onWireWithMetadata (wire)](#apidoc.element.webtorrent.torrent.prototype._onWireWithMetadata)
- description and source-code
```javascript
_onWireWithMetadata = function (wire) {
  var self = this
  var timeoutId = null

  function onChokeTimeout () {
    if (self.destroyed || wire.destroyed) return

    if (self._numQueued > 2 * (self._numConns - self.numPeers) &&
      wire.amInterested) {
      wire.destroy()
    } else {
      timeoutId = setTimeout(onChokeTimeout, CHOKE_TIMEOUT)
      if (timeoutId.unref) timeoutId.unref()
    }
  }

  var i
  function updateSeedStatus () {
    if (wire.peerPieces.buffer.length !== self.bitfield.buffer.length) return
    for (i = 0; i < self.pieces.length; ++i) {
      if (!wire.peerPieces.get(i)) return
    }
    wire.isSeeder = true
    wire.choke() // always choke seeders
  }

  wire.on('bitfield', function () {
    updateSeedStatus()
    self._update()
  })

  wire.on('have', function () {
    updateSeedStatus()
    self._update()
  })

  wire.once('interested', function () {
    wire.unchoke()
  })

  wire.once('close', function () {
    clearTimeout(timeoutId)
  })

  wire.on('choke', function () {
    clearTimeout(timeoutId)
    timeoutId = setTimeout(onChokeTimeout, CHOKE_TIMEOUT)
    if (timeoutId.unref) timeoutId.unref()
  })

  wire.on('unchoke', function () {
    clearTimeout(timeoutId)
    self._update()
  })

  wire.on('request', function (index, offset, length, cb) {
    if (length > MAX_BLOCK_LENGTH) {
      // Per spec, disconnect from peers that request >128KB
      return wire.destroy()
    }
    if (self.pieces[index]) return
    self.store.get(index, { offset: offset, length: length }, cb)
  })

  wire.bitfield(self.bitfield) // always send bitfield (required)
  wire.interested() // always start out interested

  // Send PORT message to peers that support DHT
  if (wire.peerExtensions.dht && self.client.dht && self.client.dht.listening) {
    wire.port(self.client.dht.address().port)
  }

  if (wire.type !== 'webSeed') { // do not choke on webseeds
    timeoutId = setTimeout(onChokeTimeout, CHOKE_TIMEOUT)
    if (timeoutId.unref) timeoutId.unref()
  }

  wire.isSeeder = false
  updateSeedStatus()
}
```
- example usage
```shell
...
self.bitfield = new BitField(self.pieces.length)

self.wires.forEach(function (wire) {
  // If we didn't have the metadata at the time ut_metadata was initialized for this
  // wire, we still want to make it available to the peer in case they request it.
  if (wire.ut_metadata) wire.ut_metadata.setMetadata(self.metadata)

  self._onWireWithMetadata(wire)
})

self._debug('verifying existing torrent data')
if (self._fileModtimes && self._store === FSChunkStore) {
  // don't verify if the files haven't been modified since we last checked
  self.getFileModtimes(function (err, fileModtimes) {
    if (err) return self._destroy(err)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._processParsedTorrent"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_processParsedTorrent (parsedTorrent)](#apidoc.element.webtorrent.torrent.prototype._processParsedTorrent)
- description and source-code
```javascript
_processParsedTorrent = function (parsedTorrent) {
  this._debugId = parsedTorrent.infoHash.toString('hex').substring(0, 7)

  if (this.announce) {
    // Allow specifying trackers via 'opts' parameter
    parsedTorrent.announce = parsedTorrent.announce.concat(this.announce)
  }

  if (this.client.tracker && global.WEBTORRENT_ANNOUNCE && !this.private) {
    // So 'webtorrent-hybrid' can force specific trackers to be used
    parsedTorrent.announce = parsedTorrent.announce.concat(global.WEBTORRENT_ANNOUNCE)
  }

  if (this.urlList) {
    // Allow specifying web seeds via 'opts' parameter
    parsedTorrent.urlList = parsedTorrent.urlList.concat(this.urlList)
  }

  uniq(parsedTorrent.announce)
  uniq(parsedTorrent.urlList)

  extendMutable(this, parsedTorrent)

  this.magnetURI = parseTorrent.toMagnetURI(parsedTorrent)
  this.torrentFile = parseTorrent.toTorrentFile(parsedTorrent)
}
```
- example usage
```shell
...
}
}

Torrent.prototype._onParsedTorrent = function (parsedTorrent) {
var self = this
if (self.destroyed) return

self._processParsedTorrent(parsedTorrent)

if (!self.infoHash) {
  return self._destroy(new Error('Malformed torrent data: No info hash'))
}

if (!self.path) self.path = path.join(TMP, self.infoHash)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._rechoke"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_rechoke ()](#apidoc.element.webtorrent.torrent.prototype._rechoke)
- description and source-code
```javascript
_rechoke = function () {
  var self = this
  if (!self.ready) return

  if (self._rechokeOptimisticTime > 0) self._rechokeOptimisticTime -= 1
  else self._rechokeOptimisticWire = null

  var peers = []

  self.wires.forEach(function (wire) {
    if (!wire.isSeeder && wire !== self._rechokeOptimisticWire) {
      peers.push({
        wire: wire,
        downloadSpeed: wire.downloadSpeed(),
        uploadSpeed: wire.uploadSpeed(),
        salt: Math.random(),
        isChoked: true
      })
    }
  })

  peers.sort(rechokeSort)

  var unchokeInterested = 0
  var i = 0
  for (; i < peers.length && unchokeInterested < self._rechokeNumSlots; ++i) {
    peers[i].isChoked = false
    if (peers[i].wire.peerInterested) unchokeInterested += 1
  }

  // Optimistically unchoke a peer
  if (!self._rechokeOptimisticWire && i < peers.length && self._rechokeNumSlots) {
    var candidates = peers.slice(i).filter(function (peer) { return peer.wire.peerInterested })
    var optimistic = candidates[randomInt(candidates.length)]

    if (optimistic) {
      optimistic.isChoked = false
      self._rechokeOptimisticWire = optimistic.wire
      self._rechokeOptimisticTime = RECHOKE_OPTIMISTIC_DURATION
    }
  }

  // Unchoke best peers
  peers.forEach(function (peer) {
    if (peer.wire.amChoking !== peer.isChoked) {
      if (peer.isChoked) peer.wire.choke()
      else peer.wire.unchoke()
    }
  })

  function rechokeSort (peerA, peerB) {
    // Prefer higher download speed
    if (peerA.downloadSpeed !== peerB.downloadSpeed) {
      return peerB.downloadSpeed - peerA.downloadSpeed
    }

    // Prefer higher upload speed
    if (peerA.uploadSpeed !== peerB.uploadSpeed) {
      return peerB.uploadSpeed - peerA.uploadSpeed
    }

    // Prefer unchoked
    if (peerA.wire.amChoking !== peerB.wire.amChoking) {
      return peerA.wire.amChoking ? 1 : -1
    }

    // Random order
    return peerA.salt - peerB.salt
  }
}
```
- example usage
```shell
...
if (!self.infoHash) {
  return self._destroy(new Error('Malformed torrent data: No info hash'))
}

if (!self.path) self.path = path.join(TMP, self.infoHash)

self._rechokeIntervalId = setInterval(function () {
  self._rechoke()
}, RECHOKE_INTERVAL)
if (self._rechokeIntervalId.unref) self._rechokeIntervalId.unref()

// Private 'infoHash' event allows client.add to check for duplicate torrents and
// destroy them before the normal 'infoHash' event is emitted. Prevents user
// applications from needing to deal with duplicate 'infoHash' events.
self.emit('_infoHash', self.infoHash)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._request"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_request (wire, index, hotswap)](#apidoc.element.webtorrent.torrent.prototype._request)
- description and source-code
```javascript
_request = function (wire, index, hotswap) {
  var self = this
  var numRequests = wire.requests.length
  var isWebSeed = wire.type === 'webSeed'

  if (self.bitfield.get(index)) return false

  var maxOutstandingRequests = isWebSeed
    ? Math.min(
        getPiecePipelineLength(wire, PIPELINE_MAX_DURATION, self.pieceLength),
        self.maxWebConns
      )
    : getBlockPipelineLength(wire, PIPELINE_MAX_DURATION)

  if (numRequests >= maxOutstandingRequests) return false
  // var endGame = (wire.requests.length === 0 && self.store.numMissing < 30)

  var piece = self.pieces[index]
  var reservation = isWebSeed ? piece.reserveRemaining() : piece.reserve()

  if (reservation === -1 && hotswap && self._hotswap(wire, index)) {
    reservation = isWebSeed ? piece.reserveRemaining() : piece.reserve()
  }
  if (reservation === -1) return false

  var r = self._reservations[index]
  if (!r) r = self._reservations[index] = []
  var i = r.indexOf(null)
  if (i === -1) i = r.length
  r[i] = wire

  var chunkOffset = piece.chunkOffset(reservation)
  var chunkLength = isWebSeed ? piece.chunkLengthRemaining(reservation) : piece.chunkLength(reservation)

  wire.request(index, chunkOffset, chunkLength, function onChunk (err, chunk) {
    // TODO: what is this for?
    if (!self.ready) return self.once('ready', function () { onChunk(err, chunk) })

    if (r[i] === wire) r[i] = null

    if (piece !== self.pieces[index]) return onUpdateTick()

    if (err) {
      self._debug(
        'error getting piece %s (offset: %s length: %s) from %s: %s',
        index, chunkOffset, chunkLength, wire.remoteAddress + ':' + wire.remotePort,
        err.message
      )
      isWebSeed ? piece.cancelRemaining(reservation) : piece.cancel(reservation)
      onUpdateTick()
      return
    }

    self._debug(
      'got piece %s (offset: %s length: %s) from %s',
      index, chunkOffset, chunkLength, wire.remoteAddress + ':' + wire.remotePort
    )

    if (!piece.set(reservation, chunk, wire)) return onUpdateTick()

    var buf = piece.flush()

    // TODO: might need to set self.pieces[index] = null here since sha1 is async

    sha1(buf, function (hash) {
      if (self.destroyed) return

      if (hash === self._hashes[index]) {
        if (!self.pieces[index]) return
        self._debug('piece verified %s', index)

        self.pieces[index] = null
        self._reservations[index] = null
        self.bitfield.set(index, true)

        self.store.put(index, buf)

        self.wires.forEach(function (wire) {
          wire.have(index)
        })

        // We also check 'self.destroyed' since 'torrent.destroy()' could have been
        // called in the 'torrent.on('done')' handler, triggered by '_checkDone()'.
        if (self._checkDone() && !self.destroyed) self.discovery.complete()
      } else {
        self.pieces[index] = new Piece(piece.length)
        self.emit('warning', new Error('Piece ' + index + ' failed verification'))
      }
      onUpdateTick()
    })
  })

  function onUpdateTick () {
    process.nextTick(function () { self._update() })
  }

  return true
}
```
- example usage
```shell
...
  var tried = {}
  var tries = 0
  var filter = genPieceFilterFunc(start, end, tried)

  while (tries < len) {
    piece = self._rarityMap.getRarestPiece(filter)
    if (piece < 0) break
    if (self._request(wire, piece, false)) return
    tried[piece] = true
    tries += 1
  }
} else {
  for (piece = next.to; piece >= next.from + next.offset; --piece) {
    if (!wire.peerPieces.get(piece)) continue
    if (self._request(wire, piece, false)) return
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._update"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_update ()](#apidoc.element.webtorrent.torrent.prototype._update)
- description and source-code
```javascript
_update = function () {
  var self = this
  if (self.destroyed) return

  // update wires in random order for better request distribution
  var ite = randomIterate(self.wires)
  var wire
  while ((wire = ite())) {
    self._updateWire(wire)
  }
}
```
- example usage
```shell
...
  }
  wire.isSeeder = true
  wire.choke() // always choke seeders
}

wire.on('bitfield', function () {
  updateSeedStatus()
  self._update()
})

wire.on('have', function () {
  updateSeedStatus()
  self._update()
})
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._updateInterest"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateInterest ()](#apidoc.element.webtorrent.torrent.prototype._updateInterest)
- description and source-code
```javascript
_updateInterest = function () {
  var self = this

  var prev = self._amInterested
  self._amInterested = !!self._selections.length

  self.wires.forEach(function (wire) {
    // TODO: only call wire.interested if the wire has at least one piece we need
    if (self._amInterested) wire.interested()
    else wire.uninterested()
  })

  if (prev === self._amInterested) return
  if (self._amInterested) self.emit('interested')
  else self.emit('uninterested')
}
```
- example usage
```shell
...
Torrent.prototype._updateSelections = function () {
  var self = this
  if (!self.ready || self.destroyed) return

  process.nextTick(function () {
    self._gcSelections()
  })
  self._updateInterest()
  self._update()
}

/**
 * Garbage collect selections with respect to the store's current state.
 */
Torrent.prototype._gcSelections = function () {
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._updateSelections"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateSelections ()](#apidoc.element.webtorrent.torrent.prototype._updateSelections)
- description and source-code
```javascript
_updateSelections = function () {
  var self = this
  if (!self.ready || self.destroyed) return

  process.nextTick(function () {
    self._gcSelections()
  })
  self._updateInterest()
  self._update()
}
```
- example usage
```shell
...
  self.ready = true
  self.emit('ready')

  // Files may start out done if the file was already in the store
  self._checkDone()

  // In case any selections were made before torrent was ready
  self._updateSelections()
}

Torrent.prototype.destroy = function (cb) {
  var self = this
  self._destroy(null, cb)
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._updateWire"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_updateWire (wire)](#apidoc.element.webtorrent.torrent.prototype._updateWire)
- description and source-code
```javascript
_updateWire = function (wire) {
  var self = this

  if (wire.peerChoking) return
  if (!wire.downloaded) return validateWire()

  var minOutstandingRequests = getBlockPipelineLength(wire, PIPELINE_MIN_DURATION)
  if (wire.requests.length >= minOutstandingRequests) return
  var maxOutstandingRequests = getBlockPipelineLength(wire, PIPELINE_MAX_DURATION)

  trySelectWire(false) || trySelectWire(true)

  function genPieceFilterFunc (start, end, tried, rank) {
    return function (i) {
      return i >= start && i <= end && !(i in tried) && wire.peerPieces.get(i) && (!rank || rank(i))
    }
  }

  // TODO: Do we need both validateWire and trySelectWire?
  function validateWire () {
    if (wire.requests.length) return

    var i = self._selections.length
    while (i--) {
      var next = self._selections[i]
      var piece
      if (self.strategy === 'rarest') {
        var start = next.from + next.offset
        var end = next.to
        var len = end - start + 1
        var tried = {}
        var tries = 0
        var filter = genPieceFilterFunc(start, end, tried)

        while (tries < len) {
          piece = self._rarityMap.getRarestPiece(filter)
          if (piece < 0) break
          if (self._request(wire, piece, false)) return
          tried[piece] = true
          tries += 1
        }
      } else {
        for (piece = next.to; piece >= next.from + next.offset; --piece) {
          if (!wire.peerPieces.get(piece)) continue
          if (self._request(wire, piece, false)) return
        }
      }
    }

    // TODO: wire failed to validate as useful; should we close it?
    // probably not, since 'have' and 'bitfield' messages might be coming
  }

  function speedRanker () {
    var speed = wire.downloadSpeed() || 1
    if (speed > SPEED_THRESHOLD) return function () { return true }

    var secs = Math.max(1, wire.requests.length) * Piece.BLOCK_LENGTH / speed
    var tries = 10
    var ptr = 0

    return function (index) {
      if (!tries || self.bitfield.get(index)) return true

      var missing = self.pieces[index].missing

      for (; ptr < self.wires.length; ptr++) {
        var otherWire = self.wires[ptr]
        var otherSpeed = otherWire.downloadSpeed()

        if (otherSpeed < SPEED_THRESHOLD) continue
        if (otherSpeed <= speed) continue
        if (!otherWire.peerPieces.get(index)) continue
        if ((missing -= otherSpeed * secs) > 0) continue

        tries--
        return false
      }

      return true
    }
  }

  function shufflePriority (i) {
    var last = i
    for (var j = i; j < self._selections.length && self._selections[j].priority; j++) {
      last = j
    }
    var tmp = self._selections[i]
    self._selections[i] = self._selections[last]
    self._selections[last] = tmp
  }

  function trySelectWire (hotswap) {
    if (wire.requests.length >= maxOutstandingRequests) return true
    var rank = speedRanker()

    for (var i = 0; i < self._selections.length; i++) {
      var next = self._selections[i]

      var piece
      if (self.strategy === 'rarest') {
        var start = next.from + next.offset
        var end = next.to
        var len = end - start + 1
        var tried = {}
        var tries = 0
        var filter = genPieceFilterFunc(start, end, tried, rank)

        while (tries < len) {
          piece = self._rarityMap.getRarestPiece(filter)
          if (piece < 0) break

          // request all non-reserved blocks in this piece
          while (self._request(wire, piece, self._critical[piece] || hotswap)) {}

          if (wire.requests.length < maxOutstandingRequests) {
            tried[piece] = true
            tries++
            continue
          }

          if (next.priority) shufflePriority(i)
          return true
        }
      } else {
        for (piece = next.from + next.offset; piece <= next.to; piece++) {
          if (!wire.peerPieces.get(piece) || !rank(piece)) continue

          // request all non-reserved blocks in piece
          while (self._request(wire, piece, self._critical[piece] || hotswap)) {}

          if (wire.requests.length < maxOutstan ...
```
- example usage
```shell
...
  var self = this
  if (self.destroyed) return

  // update wires in random order for better request distribution
  var ite = randomIterate(self.wires)
  var wire
  while ((wire = ite())) {
    self._updateWire(wire)
  }
}

/**
 * Attempts to update a peer's requests
 */
Torrent.prototype._updateWire = function (wire) {
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._validAddr"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_validAddr (addr)](#apidoc.element.webtorrent.torrent.prototype._validAddr)
- description and source-code
```javascript
_validAddr = function (addr) {
  var parts
  try {
    parts = addrToIPPort(addr)
  } catch (e) {
    return false
  }
  var host = parts[0]
  var port = parts[1]
  return port > 0 && port < 65535 &&
    !(host === '127.0.0.1' && port === this.client.torrentPort)
}
```
- example usage
```shell
...

Torrent.prototype._addPeer = function (peer) {
var self = this
if (self.destroyed) {
  if (typeof peer !== 'string') peer.destroy()
  return null
}
if (typeof peer === 'string' && !self._validAddr(peer)) {
  self._debug('ignoring peer: invalid %s', peer)
  return null
}

var id = (peer && peer.id) || peer
if (self._peers[id]) {
  self._debug('ignoring peer: duplicate (%s)', id)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype._verifyPieces"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>_verifyPieces ()](#apidoc.element.webtorrent.torrent.prototype._verifyPieces)
- description and source-code
```javascript
_verifyPieces = function () {
  var self = this
  parallelLimit(self.pieces.map(function (_, index) {
    return function (cb) {
      if (self.destroyed) return cb(new Error('torrent is destroyed'))

      self.store.get(index, function (err, buf) {
        if (self.destroyed) return cb(new Error('torrent is destroyed'))

        if (err) return process.nextTick(cb, null) // ignore error
        sha1(buf, function (hash) {
          if (self.destroyed) return cb(new Error('torrent is destroyed'))

          if (hash === self._hashes[index]) {
            if (!self.pieces[index]) return
            self._debug('piece verified %s', index)
            self._markVerified(index)
          } else {
            self._debug('piece invalid %s', index)
          }
          cb(null)
        })
      })
    }
  }), FILESYSTEM_CONCURRENCY, function (err) {
    if (err) return self._destroy(err)
    self._debug('done verifying')
    self._onStore()
  })
}
```
- example usage
```shell
...

    if (unchanged) {
      for (var index = 0; index < self.pieces.length; index++) {
        self._markVerified(index)
      }
      self._onStore()
    } else {
      self._verifyPieces()
    }
  })
} else {
  self._verifyPieces()
}

self.emit('metadata')
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.addPeer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>addPeer (peer)](#apidoc.element.webtorrent.torrent.prototype.addPeer)
- description and source-code
```javascript
addPeer = function (peer) {
  var self = this
  if (self.destroyed) throw new Error('torrent is destroyed')
  if (!self.infoHash) throw new Error('addPeer() must not be called before the 'infoHash' event')

  if (self.client.blocked) {
    var host
    if (typeof peer === 'string') {
      var parts
      try {
        parts = addrToIPPort(peer)
      } catch (e) {
        self._debug('ignoring peer: invalid %s', peer)
        self.emit('invalidPeer', peer)
        return false
      }
      host = parts[0]
    } else if (typeof peer.remoteAddress === 'string') {
      host = peer.remoteAddress
    }

    if (host && self.client.blocked.contains(host)) {
      self._debug('ignoring peer: blocked %s', peer)
      if (typeof peer !== 'string') peer.destroy()
      self.emit('blockedPeer', peer)
      return false
    }
  }

  var wasAdded = !!self._addPeer(peer)
  if (wasAdded) {
    self.emit('peer', peer)
  } else {
    self.emit('invalidPeer', peer)
  }
  return wasAdded
}
```
- example usage
```shell
...
function onError (err) {
  self._destroy(err)
}

function onPeer (peer) {
  // Don't create new outgoing TCP connections when torrent is done
  if (typeof peer === 'string' && self.done) return
  self.addPeer(peer)
}

function onTrackerAnnounce () {
  self.emit('trackerAnnounce')
  if (self.numPeers === 0) self.emit('noPeers', 'tracker')
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.addWebSeed"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>addWebSeed (url)](#apidoc.element.webtorrent.torrent.prototype.addWebSeed)
- description and source-code
```javascript
addWebSeed = function (url) {
  if (this.destroyed) throw new Error('torrent is destroyed')

  if (!/^https?:\/\/.+/.test(url)) {
    this.emit('warning', new Error('ignoring invalid web seed: ' + url))
    this.emit('invalidPeer', url)
    return
  }

  if (this._peers[url]) {
    this.emit('warning', new Error('ignoring duplicate web seed: ' + url))
    this.emit('invalidPeer', url)
    return
  }

  this._debug('add web seed %s', url)

  var newPeer = Peer.createWebSeedPeer(url, this)
  this._peers[newPeer.id] = newPeer
  this._peersLength += 1

  this.emit('peer', url)
}
```
- example usage
```shell
...

self._processParsedTorrent(parsedTorrent)
self.metadata = self.torrentFile

// add web seed urls (BEP19)
if (self.client.enableWebSeeds) {
  self.urlList.forEach(function (url) {
    self.addWebSeed(url)
  })
}

// start off selecting the entire torrent with low priority
if (self.pieces.length !== 0) {
  self.select(0, self.pieces.length - 1, false)
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.createServer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>createServer (requestListener)](#apidoc.element.webtorrent.torrent.prototype.createServer)
- description and source-code
```javascript
createServer = function (requestListener) {
  if (typeof Server !== 'function') throw new Error('node.js-only method')
  if (this.destroyed) throw new Error('torrent is destroyed')
  var server = new Server(this, requestListener)
  this._servers.push(server)
  return server
}
```
- example usage
```shell
...
var http = require('http')
var mime = require('mime')
var pump = require('pump')
var rangeParser = require('range-parser')
var url = require('url')

function Server (torrent, requestListener) {
var server = http.createServer(requestListener)

var sockets = []
var pendingReady = []
var closed = false

server.on('connection', onConnection)
server.on('request', onRequest)
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.critical"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>critical (start, end)](#apidoc.element.webtorrent.torrent.prototype.critical)
- description and source-code
```javascript
critical = function (start, end) {
  var self = this
  if (self.destroyed) throw new Error('torrent is destroyed')

  self._debug('critical %s-%s', start, end)

  for (var i = start; i <= end; ++i) {
    self._critical[i] = true
  }

  self._updateSelections()
}
```
- example usage
```shell
...
}

FileStream.prototype._notify = function () {
var self = this

if (!self._reading || self._missing === 0) return
if (!self._torrent.bitfield.get(self._piece)) {
  return self._torrent.critical(self._piece, self._piece + self._criticalLength)
}

if (self._notifying) return
self._notifying = true

var p = self._piece
self._torrent.store.get(p, function (err, buffer) {
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.deselect"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>deselect (start, end, priority)](#apidoc.element.webtorrent.torrent.prototype.deselect)
- description and source-code
```javascript
deselect = function (start, end, priority) {
  var self = this
  if (self.destroyed) throw new Error('torrent is destroyed')

  priority = Number(priority) || 0
  self._debug('deselect %s-%s (priority %s)', start, end, priority)

  for (var i = 0; i < self._selections.length; ++i) {
    var s = self._selections[i]
    if (s.from === start && s.to === end && s.priority === priority) {
      self._selections.splice(i, 1)
      break
    }
  }

  self._updateSelections()
}
```
- example usage
```shell
...
}

FileStream.prototype._destroy = function (err, onclose) {
  if (this.destroyed) return
  this.destroyed = true

  if (!this._torrent.destroyed) {
    this._torrent.deselect(this._startPiece, this._endPiece, true)
  }

  if (err) this.emit('error', err)
  this.emit('close')
  if (onclose) onclose()
}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>destroy (cb)](#apidoc.element.webtorrent.torrent.prototype.destroy)
- description and source-code
```javascript
destroy = function (cb) {
  var self = this
  self._destroy(null, cb)
}
```
- example usage
```shell
...
this._remove(torrentId, cb)
}

WebTorrent.prototype._remove = function (torrentId, cb) {
var torrent = this.get(torrentId)
if (!torrent) return
this.torrents.splice(this.torrents.indexOf(torrent), 1)
torrent.destroy(cb)
}

WebTorrent.prototype.address = function () {
if (!this.listening) return null
return this._tcpPool
  ? this._tcpPool.server.address()
  : { address: '0.0.0.0', family: 'IPv4', port: 0 }
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.getFileModtimes"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>getFileModtimes (cb)](#apidoc.element.webtorrent.torrent.prototype.getFileModtimes)
- description and source-code
```javascript
getFileModtimes = function (cb) {
  var self = this
  var ret = []
  parallelLimit(self.files.map(function (file, index) {
    return function (cb) {
      fs.stat(path.join(self.path, file.path), function (err, stat) {
        if (err && err.code !== 'ENOENT') return cb(err)
        ret[index] = stat && stat.mtime.getTime()
        cb(null)
      })
    }
  }), FILESYSTEM_CONCURRENCY, function (err) {
    self._debug('done getting file modtimes')
    cb(err, ret)
  })
}
```
- example usage
```shell
...

    self._onWireWithMetadata(wire)
  })

  self._debug('verifying existing torrent data')
  if (self._fileModtimes && self._store === FSChunkStore) {
    // don't verify if the files haven't been modified since we last checked
    self.getFileModtimes(function (err, fileModtimes) {
if (err) return self._destroy(err)

var unchanged = self.files.map(function (_, index) {
  return fileModtimes[index] === self._fileModtimes[index]
}).every(function (x) {
  return x
})
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.load"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>load (streams, cb)](#apidoc.element.webtorrent.torrent.prototype.load)
- description and source-code
```javascript
load = function (streams, cb) {
  var self = this
  if (self.destroyed) throw new Error('torrent is destroyed')
  if (!self.ready) return self.once('ready', function () { self.load(streams, cb) })

  if (!Array.isArray(streams)) streams = [ streams ]
  if (!cb) cb = noop

  var readable = new MultiStream(streams)
  var writable = new ChunkStoreWriteStream(self.store, self.pieceLength)

  pump(readable, writable, function (err) {
    if (err) return cb(err)
    self.pieces.forEach(function (piece, index) {
      self.pieces[index] = null
      self._reservations[index] = null
      self.bitfield.set(index, true)
    })
    self._checkDone()
    cb(null)
  })
}
```
- example usage
```shell
...
    })
  })
})

function onTorrent (torrent) {
  var tasks = [
    function (cb) {
      torrent.load(streams, cb)
    }
  ]
  if (self.dht) {
    tasks.push(function (cb) {
      torrent.once('dhtAnnounce', cb)
    })
  }
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.pause"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>pause ()](#apidoc.element.webtorrent.torrent.prototype.pause)
- description and source-code
```javascript
pause = function () {
  if (this.destroyed) return
  this._debug('pause')
  this.paused = true
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.removePeer"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>removePeer (peer)](#apidoc.element.webtorrent.torrent.prototype.removePeer)
- description and source-code
```javascript
removePeer = function (peer) {
  var self = this
  var id = (peer && peer.id) || peer
  peer = self._peers[id]

  if (!peer) return

  this._debug('removePeer %s', id)

  delete self._peers[id]
  self._peersLength -= 1

  peer.destroy()

  // If torrent swarm was at capacity before, try to open a new connection now
  self._drain()
}
```
- example usage
```shell
...
    arrayRemove(swarm.wires, swarm.wires.indexOf(wire))
  }
  if (conn) {
    conn.on('error', noop)
    conn.destroy()
  }
  if (wire) wire.destroy()
  if (swarm) swarm.removePeer(self.id)
}

function noop () {}
...
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.resume"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>resume ()](#apidoc.element.webtorrent.torrent.prototype.resume)
- description and source-code
```javascript
resume = function () {
  if (this.destroyed) return
  this._debug('resume')
  this.paused = false
  this._drain()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.torrent.prototype.select"></a>[function <span class="apidocSignatureSpan">webtorrent.torrent.prototype.</span>select (start, end, priority, notify)](#apidoc.element.webtorrent.torrent.prototype.select)
- description and source-code
```javascript
select = function (start, end, priority, notify) {
  var self = this
  if (self.destroyed) throw new Error('torrent is destroyed')

  if (start < 0 || end < start || self.pieces.length <= end) {
    throw new Error('invalid selection ', start, ':', end)
  }
  priority = Number(priority) || 0

  self._debug('select %s-%s (priority %s)', start, end, priority)

  self._selections.push({
    from: start,
    to: end,
    offset: 0,
    priority: priority,
    notify: notify || noop
  })

  self._selections.sort(function (a, b) {
    return b.priority - a.priority
  })

  self._updateSelections()
}
```
- example usage
```shell
...
    }
    return downloaded
  }
})

File.prototype.select = function (priority) {
  if (this.length === 0) return
  this._torrent.select(this._startPiece, this._endPiece, priority)
}

File.prototype.deselect = function () {
  if (this.length === 0) return
  this._torrent.deselect(this._startPiece, this._endPiece, false)
}
...
```



# <a name="apidoc.module.webtorrent.webconn"></a>[module webtorrent.webconn](#apidoc.module.webtorrent.webconn)

#### <a name="apidoc.element.webtorrent.webconn.webconn"></a>[function <span class="apidocSignatureSpan">webtorrent.</span>webconn (url, torrent)](#apidoc.element.webtorrent.webconn.webconn)
- description and source-code
```javascript
function WebConn(url, torrent) {
  Wire.call(this)

  this.url = url
  this.webPeerId = sha1.sync(url)
  this._torrent = torrent

  this._init()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webtorrent.webconn.super_"></a>[function <span class="apidocSignatureSpan">webtorrent.webconn.</span>super_ ()](#apidoc.element.webtorrent.webconn.super_)
- description and source-code
```javascript
function Wire() {
  if (!(this instanceof Wire)) return new Wire()
  stream.Duplex.call(this)

  this._debugId = randombytes(4).toString('hex')
  this._debug('new wire')

  this.peerId = null // remote peer id (hex string)
  this.peerIdBuffer = null // remote peer id (buffer)
  this.type = null // connection type ('webrtc', 'tcpIncoming', 'tcpOutgoing', 'webSeed')

  this.amChoking = true // are we choking the peer?
  this.amInterested = false // are we interested in the peer?

  this.peerChoking = true // is the peer choking us?
  this.peerInterested = false // is the peer interested in us?

  // The largest torrent that I know of (the Geocities archive) is ~641 GB and has
  // ~41,000 pieces. Therefore, cap bitfield to 10x larger (400,000 bits) to support all
  // possible torrents but prevent malicious peers from growing bitfield to fill memory.
  this.peerPieces = new BitField(0, { grow: BITFIELD_GROW })

  this.peerExtensions = {}

  this.requests = [] // outgoing
  this.peerRequests = [] // incoming

  this.extendedMapping = {} // number -> string, ex: 1 -> 'ut_metadata'
  this.peerExtendedMapping = {} // string -> number, ex: 9 -> 'ut_metadata'

  // The extended handshake to send, minus the "m" field, which gets automatically
  // filled from 'this.extendedMapping'
  this.extendedHandshake = {}

  this.peerExtendedHandshake = {} // remote peer's extended handshake

  this._ext = {}  // string -> function, ex 'ut_metadata' -> ut_metadata()
  this._nextExt = 1

  this.uploaded = 0
  this.downloaded = 0
  this.uploadSpeed = speedometer()
  this.downloadSpeed = speedometer()

  this._keepAliveInterval = null
  this._timeout = null
  this._timeoutMs = 0

  this.destroyed = false // was the wire ended by calling 'destroy'?
  this._finished = false

  this._parserSize = 0 // number of needed bytes to parse next message from remote peer
  this._parser = null // function to call once 'this._parserSize' bytes are available

  this._buffer = [] // incomplete message data
  this._bufferSize = 0 // cached total length of buffers in 'this._buffer'

  this.on('finish', this._onFinish)

  this._parseHandshake()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webtorrent.webconn.prototype"></a>[module webtorrent.webconn.prototype](#apidoc.module.webtorrent.webconn.prototype)

#### <a name="apidoc.element.webtorrent.webconn.prototype._init"></a>[function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>_init ()](#apidoc.element.webtorrent.webconn.prototype._init)
- description and source-code
```javascript
_init = function () {
  var self = this
  self.setKeepAlive(true)

  self.once('handshake', function (infoHash, peerId) {
    if (self.destroyed) return
    self.handshake(infoHash, self.webPeerId)
    var numPieces = self._torrent.pieces.length
    var bitfield = new BitField(numPieces)
    for (var i = 0; i <= numPieces; i++) {
      bitfield.set(i, true)
    }
    self.bitfield(bitfield)
  })

  self.once('interested', function () {
    debug('interested')
    self.unchoke()
  })

  self.on('uninterested', function () { debug('uninterested') })
  self.on('choke', function () { debug('choke') })
  self.on('unchoke', function () { debug('unchoke') })
  self.on('bitfield', function () { debug('bitfield') })

  self.on('request', function (pieceIndex, offset, length, callback) {
    debug('request pieceIndex=%d offset=%d length=%d', pieceIndex, offset, length)
    self.httpRequest(pieceIndex, offset, length, callback)
  })
}
```
- example usage
```shell
...
function WebConn (url, torrent) {
Wire.call(this)

this.url = url
this.webPeerId = sha1.sync(url)
this._torrent = torrent

this._init()
}

WebConn.prototype._init = function () {
var self = this
self.setKeepAlive(true)

self.once('handshake', function (infoHash, peerId) {
...
```

#### <a name="apidoc.element.webtorrent.webconn.prototype.destroy"></a>[function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>destroy ()](#apidoc.element.webtorrent.webconn.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  Wire.prototype.destroy.call(this)
  this._torrent = null
}
```
- example usage
```shell
...
this._remove(torrentId, cb)
}

WebTorrent.prototype._remove = function (torrentId, cb) {
var torrent = this.get(torrentId)
if (!torrent) return
this.torrents.splice(this.torrents.indexOf(torrent), 1)
torrent.destroy(cb)
}

WebTorrent.prototype.address = function () {
if (!this.listening) return null
return this._tcpPool
  ? this._tcpPool.server.address()
  : { address: '0.0.0.0', family: 'IPv4', port: 0 }
...
```

#### <a name="apidoc.element.webtorrent.webconn.prototype.httpRequest"></a>[function <span class="apidocSignatureSpan">webtorrent.webconn.prototype.</span>httpRequest (pieceIndex, offset, length, cb)](#apidoc.element.webtorrent.webconn.prototype.httpRequest)
- description and source-code
```javascript
httpRequest = function (pieceIndex, offset, length, cb) {
  var self = this
  var pieceOffset = pieceIndex * self._torrent.pieceLength
  var rangeStart = pieceOffset + offset<span class="apidocCodeCommentSpan"> /* offset within whole torrent */
</span>  var rangeEnd = rangeStart + length - 1

  // Web seed URL format:
  // For single-file torrents, make HTTP range requests directly to the web seed URL
  // For multi-file torrents, add the torrent folder and file name to the URL
  var files = self._torrent.files
  var requests
  if (files.length <= 1) {
    requests = [{
      url: self.url,
      start: rangeStart,
      end: rangeEnd
    }]
  } else {
    var requestedFiles = files.filter(function (file) {
      return file.offset <= rangeEnd && (file.offset + file.length) > rangeStart
    })
    if (requestedFiles.length < 1) {
      return cb(new Error('Could not find file corresponnding to web seed range request'))
    }

    requests = requestedFiles.map(function (requestedFile) {
      var fileEnd = requestedFile.offset + requestedFile.length - 1
      var url = self.url +
        (self.url[self.url.length - 1] === '/' ? '' : '/') +
        requestedFile.path
      return {
        url: url,
        fileOffsetInRange: Math.max(requestedFile.offset - rangeStart, 0),
        start: Math.max(rangeStart - requestedFile.offset, 0),
        end: Math.min(fileEnd, rangeEnd - requestedFile.offset)
      }
    })
  }

  // Now make all the HTTP requests we need in order to load this piece
  // Usually that's one requests, but sometimes it will be multiple
  // Send requests in parallel and wait for them all to come back
  var numRequestsSucceeded = 0
  var hasError = false

  var ret
  if (requests.length > 1) {
    ret = Buffer.alloc(length)
  }

  requests.forEach(function (request) {
    var url = request.url
    var start = request.start
    var end = request.end
    debug(
      'Requesting url=%s pieceIndex=%d offset=%d length=%d start=%d end=%d',
      url, pieceIndex, offset, length, start, end
    )
    var opts = {
      url: url,
      method: 'GET',
      headers: {
        'user-agent': 'WebTorrent/' + VERSION + ' (https://webtorrent.io)',
        range: 'bytes=' + start + '-' + end
      }
    }
    function onResponse (res, data) {
      if (res.statusCode < 200 || res.statusCode >= 300) {
        hasError = true
        return cb(new Error('Unexpected HTTP status code ' + res.statusCode))
      }
      debug('Got data of length %d', data.length)

      if (requests.length === 1) {
        // Common case: fetch piece in a single HTTP request, return directly
        cb(null, data)
      } else {
        // Rare case: reconstruct multiple HTTP requests across 2+ files into one
        // piece buffer
        data.copy(ret, request.fileOffsetInRange)
        if (++numRequestsSucceeded === requests.length) {
          cb(null, ret)
        }
      }
    }
    get.concat(opts, function (err, res, data) {
      if (hasError) return
      if (err) {
        // Browsers allow HTTP redirects for simple cross-origin
        // requests but not for requests that require preflight.
        // Use a simple request to unravel any redirects and get the
        // final URL.  Retry the original request with the new URL if
        // it's different.
        //
        // This test is imperfect but it's simple and good for common
        // cases.  It catches all cross-origin cases but matches a few
        // same-origin cases too.
        if (typeof window === 'undefined' || url.startsWith(window.location.origin + '/')) {
          hasError = true
          return cb(err)
        }

        return get.head(url, function (errHead, res) {
          if (hasError) return
          if (errHead) {
            hasError = true
            return cb(errHead)
          }
          if (res.statusCode < 200 || res.statusCode >= 300) {
            hasError = true
            return cb(new Error('Unexpected HTTP status code ' + res.statusCode))
          }
          if (res.url === url) {
            hasError = true
            return cb(err)
          }

          opts.url = res.url ...
```
- example usage
```shell
...
self.on('uninterested', function () { debug('uninterested') })
self.on('choke', function () { debug('choke') })
self.on('unchoke', function () { debug('unchoke') })
self.on('bitfield', function () { debug('bitfield') })

self.on('request', function (pieceIndex, offset, length, callback) {
  debug('request pieceIndex=%d offset=%d length=%d', pieceIndex, offset, length)
  self.httpRequest(pieceIndex, offset, length, callback)
})
}

WebConn.prototype.httpRequest = function (pieceIndex, offset, length, cb) {
var self = this
var pieceOffset = pieceIndex * self._torrent.pieceLength
var rangeStart = pieceOffset + offset /* offset within whole torrent */
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
