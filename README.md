# start-server-and-test

> Starts server, waits for URL, then runs test command; when the tests end, shuts down server

[![NPM][npm-icon] ][npm-url]

[![Build status][ci-image] ][ci-url]
[![semantic-release][semantic-image] ][semantic-url]
[![js-standard-style][standard-image]][standard-url]

## Install

Requires [Node](https://nodejs.org/en/) version 6 or above.

```sh
npm install --save-dev start-server-and-test
```

## Use

This command is meant to be used with NPM script commands. If you have a "start server",
and "test" script names for example, you can start the server, wait for a url to respond,
then run tests. When the test process exits, the server is shut down.

```json
{
    "scripts": {
        "start-server": "npm start",
        "test": "mocha e2e-spec.js",
        "ci": "start-server-and-test start-server http://localhost:8080 test"
    }
}
```

To execute all tests simply run `npm run ci`

### Options

If you use convention and name your scripts "start" and "test" you can simply provide URL

```json
{
    "scripts": {
        "start": "npm start",
        "test": "mocha e2e-spec.js",
        "ci": "start-server-and-test http://localhost:8080"
    }
}
```

### Debugging

To see diagnostic messages, run with environment variable `DEBUG=start-server-and-test`

### Small print

Author: Gleb Bahmutov &lt;gleb.bahmutov@gmail.com&gt; &copy; 2017

* [@bahmutov](https://twitter.com/bahmutov)
* [glebbahmutov.com](https://glebbahmutov.com)
* [blog](https://glebbahmutov.com/blog)

License: MIT - do anything with the code, but don't blame me if it does not work.

Support: if you find any problems with this module, email / tweet /
[open issue](https://github.com/bahmutov/start-server-and-test/issues) on Github

## MIT License

Copyright (c) 2017 Gleb Bahmutov &lt;gleb.bahmutov@gmail.com&gt;

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

[npm-icon]: https://nodei.co/npm/start-server-and-test.svg?downloads=true
[npm-url]: https://npmjs.org/package/start-server-and-test
[ci-image]: https://travis-ci.org/bahmutov/start-server-and-test.svg?branch=master
[ci-url]: https://travis-ci.org/bahmutov/start-server-and-test
[semantic-image]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-url]: https://github.com/semantic-release/semantic-release
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg
[standard-url]: http://standardjs.com/
