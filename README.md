# npmdoc-seaport

#### api documentation for  [seaport (v2.0.9)](https://github.com/substack/seaport)  [![npm package](https://img.shields.io/npm/v/npmdoc-seaport.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-seaport) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-seaport.svg)](https://travis-ci.org/npmdoc/node-npmdoc-seaport)

#### service registry and port assignment for clusters

[![NPM](https://nodei.co/npm/seaport.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/seaport)

- [https://npmdoc.github.io/node-npmdoc-seaport/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-seaport/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-seaport/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-seaport/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "James Halliday",
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
            "name": "substack"
        }
    ],
    "name": "seaport",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
