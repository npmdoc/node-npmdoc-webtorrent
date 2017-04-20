# npmdoc-webtorrent

#### api documentation for  [webtorrent (v0.98.18)](https://webtorrent.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-webtorrent.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webtorrent) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webtorrent.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webtorrent)

#### Streaming torrent client

[![NPM](https://nodei.co/npm/webtorrent.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/webtorrent)

- [https://npmdoc.github.io/node-npmdoc-webtorrent/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-webtorrent/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webtorrent/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webtorrent/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "webtorrent",
    "description": "Streaming torrent client",
    "version": "0.98.18",
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
    "engines": {
        "node": ">=4"
    },
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
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
