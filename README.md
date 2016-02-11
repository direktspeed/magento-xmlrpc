# Magento XML-RPC API Wrapper

This wrapper lets you talk to Magento via XML-RPC.

It is a minimally modified version of `magento` and `magento-api`, which incorrectly advertise as being SOAP clients.

## Installation

`npm install magento-xmlrpc`

## Usage

```js
var MagentoAPI = require('magento-xmlrpc');
var magento = new MagentoAPI({
  host: 'your.host',
  port: 80,
  path: '/api/xmlrpc/',
  login: 'your_username',
  pass: 'your_pass'
});

magento.login(function(err, sessId) {
  if (err) {
    // deal with error
    return;
  }

  // use magento
});
```

If need be, you can manually change the session id.

```js
magento.changeSession(newSessionId);
```

All of the API methods take an object of params as the first argument, and a callback as the second.

Or, if no params are sent, just a callback as the first argument.

## Methods
[Read the manual on Github](https://github.com/lobot-io/magento-xmlrpc/blob/master/MANUAL.md)
