##HTTP Server test

A test script for testing h5bp server configs

##Dependencies

 * Node.js
 * mocha

##Usage

To test on localhost, where localhost points at the contents of the fixtures/content folder:

    $ mocha

To test anywhere else upload the files:

    $ rsync -rv fixtures someserver:/var/www/example.com/public/

And use the environment variable `TEST_BASE_URL` to tell the test suite where the files are:

    $ TEST_BASE_URL=https://example.com/fixtures/content mocha
