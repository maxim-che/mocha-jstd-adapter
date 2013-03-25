Mocha Adapter for [JsTestDriver][jstd]
========================================

Author
------

* Jan Prachař (jan@prachar.eu)

Requirements
------------

 - [JsTestDriver (JSTD)][jstd]
 - [Mocha][mocha] (browser version – [mocha.js][mocha.js])
 - Any assertion library (e.g. [Chai][chai]: browser version – [chai.js][chai.js])

Usage
-----

Update your `jsTestDriver.conf` file (see [wiki page][jstd-conf] for more info)  by prepending the Mocha and assertion library and the adapter's source files.

For example:

	load:
    - "lib/mocha.js"
	- "lib/chai.js"
    - "lib/MochaAdapter.js"
    - "your_source_files.js"

	test:
    - "your_test_files.js"

Then you must setup Mocha and assertion library like for use in the browser, i.e. tell Mocha which interface you wish to use. A typical setup might look like the following.

	mocha.setup('bdd');
	expect = chai.expect;


Directory Layout
----------------
 
 - src: The adapter source code. Intent is to match interface with interface.
 - src-test: The test files that verifies that the adapter works as intended.

Changes
-------
 * 0.1 - ? Initial release


[jstd]: http://code.google.com/p/js-test-driver
[jstd-conf]: http://code.google.com/p/js-test-driver/wiki/ConfigurationFile
[mocha]: https://github.com/visionmedia/mocha 
[mocha.js]: https://github.com/visionmedia/mocha/blob/master/mocha.js
[chai]: https://github.com/chaijs/chai
[chai.js]: https://github.com/chaijs/chai/blob/master/chai.js
