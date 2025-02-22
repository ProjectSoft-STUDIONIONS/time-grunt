## Deprecated

Deprecated because Grunt is practically unmaintained. Move on to something better. This package will continue to work with Grunt v1, but it will not receive any updates.

---

# time-grunt [![Build Status](https://travis-ci.org/sindresorhus/time-grunt.svg?branch=master)](https://travis-ci.org/sindresorhus/time-grunt)

> Display the elapsed execution time of [grunt](http://gruntjs.com) tasks

![](screenshot.png)


## Install

```
$ npm install --save-dev https://github.com/ProjectSoft-STUDIONIONS/time-grunt.git
```


## Usage

```js
// Gruntfile.js
module.exports = grunt => {
	// require it at the top and pass in the grunt instance
	require('time-grunt')(grunt);

	grunt.initConfig();
}
```


## Optional callback

If you want to collect the timing stats for your own use, pass in a callback:

```js
require('time-grunt')(grunt, (stats, done) => {
	// do whatever you want with the stats
	uploadReport(stats);

	// be sure to let grunt know when to exit
	done();
});
```


## Clean layout

The `watch` task and tasks that take less than 1% of the total time are hidden to reduce clutter.

Run grunt with `grunt --verbose` to see all tasks.

Run grunt with `grunt --quiet` to quiet all tasks including time-grunt.


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
