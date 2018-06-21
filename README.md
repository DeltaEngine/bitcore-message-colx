# Colx Message Verification and Signing for Bitcore-Colx

bitcore-message-colx adds support for verifying and signing colx messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-colx repo](https://github.com/deltaengine/bitcore-colx) for more information.

## Getting Started

```sh
npm install bitcore-message-colx
```

```sh
bower install bitcore-message-colx
```

To sign a message:

```javascript
var bitcore = require('colossuscore-lib');
var Message = require('bitcore-message-colx');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/deltaengine/bitcore-colx/blob/master/CONTRIBUTING.md) on the main bitcore-colx repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

