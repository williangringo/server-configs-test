## [WIP] Test suite for the H5BP Server Configs

[![Build Status](https://travis-ci.org/h5bp/server-configs-test.svg)](https://travis-ci.org/h5bp/server-configs-test)
[![devDependency Status](https://david-dm.org/h5bp/server-configs-test/dev-status.svg)](https://david-dm.org/h5bp/server-configs-test#info=devDependencies)

Test suite for the H5BP [Server Configs](https://github.com/h5bp/server-configs).

## Setup

1. Install [`Node.js` and `npm`](http://nodejs.org/download/).
2. Run `npm install`.

## Usage

To test for `localhost`, where `localhost` points at the contents of the
`fixtures/` folder:

```bash
$ npm test
```

To test anywhere else upload the files:

```bash
$ rsync -rv src/fixtures someserver:/var/www/example.com/public/
```

then, tell `npm` where the files are and run the tests:

```bash
$ npm config set h5bp:url <URL> && npm run <TEST_NAME>
```

e.g.:

```bash
$ npm config set h5bp:url "http://example.com/fixtures" && npm run test
```
