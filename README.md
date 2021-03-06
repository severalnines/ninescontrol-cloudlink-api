# CloudLink API

An API to make requests to [CloudLink](https://github.com/simon-s9/s9s-cloudlink) service.

  [![Version][npm-image]][npm-url]
  [![Build][travis-image]][travis-url]
  [![Documentation][document-image]][document-url]

* [Documentation](https://cdn.rawgit.com/simon-s9/s9s-cloudlink-api/v1.0.21/docs/index.html)
* [Installation](#installation)
* [Examples](#examples)

## Installation
```
npm install --save s9s-cloudlink-api
```

## Examples
```javascript
const CloudlinkApi = require('s9s-cloudlink-api');
const api = new CloudlinkApi({
    cloud: 'aws',
    server: {
        host: '127.0.0.1',
        port: 3000
    },
    auth: {
        accessKeyId: '...',
        secretAccessKey: '...',
        region: 'eu-central-1'
    }
});

api
    .listInstances()
    .then((instances) => {
        console.log('resolve', instances);
    })
    .catch((error) => {
        console.log('reject', error);
    });
```

## License
Copyright (c) 2016 Severalnines AB


Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[npm-image]: https://img.shields.io/npm/v/s9s-cloudlink-api.svg?label=version
[npm-url]: https://npmjs.org/package/s9s-cloudlink-api
[travis-image]: https://travis-ci.org/simon-s9/s9s-cloudlink-api.svg?branch=master
[travis-url]: https://travis-ci.org/simon-s9/s9s-cloudlink-api
[document-image]: https://rawgit.com/simon-s9/s9s-cloudlink-api/v1.0.21/docs/badge.svg
[document-url]: https://github.com/simon-s9/s9s-cloudlink-api/releases
