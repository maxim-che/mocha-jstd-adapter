Mocha Adapter for [JsTestDriver][jstd]
========================================

Author
------

* Jan Prachař (jan@prachar.eu)

Requirements
------------

 - [JsTestDriver (JSTD)][jstd]
 - [Mocha][mocha]

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
