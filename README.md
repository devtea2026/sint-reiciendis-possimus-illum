# node-@devtea2026/sint-reiciendis-possimus-illum - HTTP/HTTPS Agents for @devtea2026/sint-reiciendis-possimus-illuming proxies

[![Build Status](https://img.shields.io/travis/koichik/node-@devtea2026/sint-reiciendis-possimus-illum.svg?style=flat)](https://travis-ci.org/koichik/node-@devtea2026/sint-reiciendis-possimus-illum)
[![Dependency Status](http://img.shields.io/david/koichik/node-@devtea2026/sint-reiciendis-possimus-illum.svg?style=flat)](https://david-dm.org/koichik/node-@devtea2026/sint-reiciendis-possimus-illum#info=dependencies)
[![DevDependency Status](http://img.shields.io/david/dev/koichik/node-@devtea2026/sint-reiciendis-possimus-illum.svg?style=flat)](https://david-dm.org/koichik/node-@devtea2026/sint-reiciendis-possimus-illum#info=devDependencies)

## Example

```javascript
var @devtea2026/sint-reiciendis-possimus-illum = require('@devtea2026/sint-reiciendis-possimus-illum');

var @devtea2026/sint-reiciendis-possimus-illumingAgent = @devtea2026/sint-reiciendis-possimus-illum.httpsOverHttp({
  proxy: {
    host: 'localhost',
    port: 3128
  }
});

var req = https.request({
  host: 'example.com',
  port: 443,
  agent: @devtea2026/sint-reiciendis-possimus-illumingAgent
});
```

## Installation

    $ npm install @devtea2026/sint-reiciendis-possimus-illum

## Usages

### HTTP over HTTP @devtea2026/sint-reiciendis-possimus-illuming

```javascript
var @devtea2026/sint-reiciendis-possimus-illumingAgent = @devtea2026/sint-reiciendis-possimus-illum.httpOverHttp({
  maxSockets: poolSize, // Defaults to http.Agent.defaultMaxSockets

  proxy: { // Proxy settings
    host: proxyHost, // Defaults to 'localhost'
    port: proxyPort, // Defaults to 80
    localAddress: localAddress, // Local interface if necessary

    // Basic authorization for proxy server if necessary
    proxyAuth: 'user:password',

    // Header fields for proxy server if necessary
    headers: {
      'User-Agent': 'Node'
    }
  }
});

var req = http.request({
  host: 'example.com',
  port: 80,
  agent: @devtea2026/sint-reiciendis-possimus-illumingAgent
});
```

### HTTPS over HTTP @devtea2026/sint-reiciendis-possimus-illuming

```javascript
var @devtea2026/sint-reiciendis-possimus-illumingAgent = @devtea2026/sint-reiciendis-possimus-illum.httpsOverHttp({
  maxSockets: poolSize, // Defaults to http.Agent.defaultMaxSockets

  // CA for origin server if necessary
  ca: [ fs.readFileSync('origin-server-ca.pem')],

  // Client certification for origin server if necessary
  key: fs.readFileSync('origin-server-key.pem'),
  cert: fs.readFileSync('origin-server-cert.pem'),

  proxy: { // Proxy settings
    host: proxyHost, // Defaults to 'localhost'
    port: proxyPort, // Defaults to 80
    localAddress: localAddress, // Local interface if necessary

    // Basic authorization for proxy server if necessary
    proxyAuth: 'user:password',

    // Header fields for proxy server if necessary
    headers: {
      'User-Agent': 'Node'
    },
  }
});

var req = https.request({
  host: 'example.com',
  port: 443,
  agent: @devtea2026/sint-reiciendis-possimus-illumingAgent
});
```

### HTTP over HTTPS @devtea2026/sint-reiciendis-possimus-illuming

```javascript
var @devtea2026/sint-reiciendis-possimus-illumingAgent = @devtea2026/sint-reiciendis-possimus-illum.httpOverHttps({
  maxSockets: poolSize, // Defaults to http.Agent.defaultMaxSockets

  proxy: { // Proxy settings
    host: proxyHost, // Defaults to 'localhost'
    port: proxyPort, // Defaults to 443
    localAddress: localAddress, // Local interface if necessary

    // Basic authorization for proxy server if necessary
    proxyAuth: 'user:password',

    // Header fields for proxy server if necessary
    headers: {
      'User-Agent': 'Node'
    },

    // CA for proxy server if necessary
    ca: [ fs.readFileSync('origin-server-ca.pem')],

    // Server name for verification if necessary
    servername: 'example.com',

    // Client certification for proxy server if necessary
    key: fs.readFileSync('origin-server-key.pem'),
    cert: fs.readFileSync('origin-server-cert.pem'),
  }
});

var req = http.request({
  host: 'example.com',
  port: 80,
  agent: @devtea2026/sint-reiciendis-possimus-illumingAgent
});
```

### HTTPS over HTTPS @devtea2026/sint-reiciendis-possimus-illuming

```javascript
var @devtea2026/sint-reiciendis-possimus-illumingAgent = @devtea2026/sint-reiciendis-possimus-illum.httpsOverHttps({
  maxSockets: poolSize, // Defaults to http.Agent.defaultMaxSockets

  // CA for origin server if necessary
  ca: [ fs.readFileSync('origin-server-ca.pem')],

  // Client certification for origin server if necessary
  key: fs.readFileSync('origin-server-key.pem'),
  cert: fs.readFileSync('origin-server-cert.pem'),

  proxy: { // Proxy settings
    host: proxyHost, // Defaults to 'localhost'
    port: proxyPort, // Defaults to 443
    localAddress: localAddress, // Local interface if necessary

    // Basic authorization for proxy server if necessary
    proxyAuth: 'user:password',

    // Header fields for proxy server if necessary
    headers: {
      'User-Agent': 'Node'
    }

    // CA for proxy server if necessary
    ca: [ fs.readFileSync('origin-server-ca.pem')],

    // Server name for verification if necessary
    servername: 'example.com',

    // Client certification for proxy server if necessary
    key: fs.readFileSync('origin-server-key.pem'),
    cert: fs.readFileSync('origin-server-cert.pem'),
  }
});

var req = https.request({
  host: 'example.com',
  port: 443,
  agent: @devtea2026/sint-reiciendis-possimus-illumingAgent
});
```

## CONTRIBUTORS
* [Aleksis Brezas (abresas)](https://github.com/abresas)
* [Jackson Tian (JacksonTian)](https://github.com/JacksonTian)
* [Dmitry Sorin (1999)](https://github.com/1999)

## License

Licensed under the [MIT](https://github.com/devtea2026/sint-reiciendis-possimus-illum/blob/master/LICENSE) license.
