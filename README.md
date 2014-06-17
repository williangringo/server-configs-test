## Test suite for the H5BP server configs

A test script for testing H5BP server configs

## Setup

1. Install [`Node.js` and `npm`](http://nodejs.org/download/).
2. Run `npm install`.

##Usage

To test on localhost, where localhost points at the contents of the fixtures/content folder:

    $ npm test

To test anywhere else upload the files:

    $ rsync -rv fixtures someserver:/var/www/example.com/public/

tell `npm` where the files are and run the tests:

    $ npm config set h5bp:url <URL> && npm run <TEST_NAME>

e.g.:

    $ npm config set h5bp:url "http://192.168.2.100/content" && npm run test
