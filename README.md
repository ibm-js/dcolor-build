# dcolor-build

Build version of [ibm-js/dcolor](https://github.com/ibm-js/dcolor).

## Status

No official release yet.

## Installation

_Bower_ release installation:

    $ bower install dcolor-build

_Manual_ master installation:

    $ git clone git://github.com/ibm-js/dcolor-build.git

Then install dependencies with bower (or manually from github if you prefer to):

	$ cd dcolor-build
	$ bower install


## How to use

To load the minified layer you need to wrap your main `require` call with another `require`, requiring `"dcolor-build/layer"`. Then you should continue to
refer to modules with `"dcolor/foo"`.

For example, this:
```
require(["app/main", "dcolor/foo"], function() {
	...
});
```
Becomes:
```
require(["dcolor-build/layer"], function() {
	require(["app/main", "dcolor/foo"], function() {
		...
	});
});
```

## Licensing

This project is distributed by the Dojo Foundation and licensed under the ["New" BSD License](./LICENSE).
All contributions require a [Dojo Foundation CLA](http://dojofoundation.org/about/claForm).
