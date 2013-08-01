# Counter.js

A _simple_ number counter in JavaScript as a jQuery plugin.
It counts the number set on an element using an easing effect.

## Example

The index.html file contains a working example of the counter.

## Usage

__Simplest implementation:__

```html
<!-- HTML -->
<div id="counter">1024</div>
```

```javascript
// JavaScript
$("#counter").counter();
```

__With some more options:__

```javascript
// JavaScript
$("#counter").counter({
  autoStart: false,         // true/false, default: true
  duration: 1000,           // milliseconds, default: 1500
  startAt: 1,               // start counting at this number, default: 0
  placeholder: "?",         // replace the number with this before counting,
                            // most useful with autoStart: false. default: 0
  easing: "swing",          // see http://gsgd.co.uk/sandbox/jquery/easing
                            // for all available effects, see visual examples:
                            // http://easings.net
                            // default: "easeOutQuad"
  onStart: function() {},   // callback on start of the counting
  onComplete: function() {} // callback on completion of the counting
});
```

## Installation

If you're just interested in just using the script then copy the
`js/counter.min.js` file in your project.
Then add the libraries as described in `Requirements` below.

## Requirements

You will need two libraries, jQuery (should work with v2, v1.10 and v1.9)
and the jQuery easing plugin (v1.3).

Make sure to add these files to your project in this order:

```javascript
jquery.js        // Download from: http://jquery.com
jquery.easing.js // Download from: http://gsgd.co.uk/sandbox/jquery/easing/
counter.js       // Is located in this repository under `js/counter.js`
                 // minified version is also available
```

_(I don't recommend you using the `js/jquery.js` and `js/jquery.easing.js` files
that are available in this repository in your project.
Instead download the latest ones from [jquery.com](http://jquery.com/) and
[gsgd.co.uk (jQuery.easing)](http://gsgd.co.uk/sandbox/jquery/easing/).)_

## Contributing

Want to help make this better? Or just modify it? Here's how:

### Requirements

For development you will need a CoffeeScript compiler and JavaScript minifier.
I use the one in [Node.js](http://nodejs.org).
For minification I use [UglifyJS2](https://github.com/mishoo/UglifyJS2).

### Compilation

Once you modified the CoffeeScript you will need to compile it to JavaScript.
There's a `Makefile` available in the repo to do so.

If you like entering commands in the terminal more, use one of these commands:

__One time compilation:__

`coffee --output js/ --compile js/counter.coffee`

__Compilation on save:__

`coffee --watch --compile ./js/counter.coffee`

### Testing

This project needs test coverage and I haven't gotten around to it yet. ;)

## License

Counter.js released under the MIT License. See the bundled LICENSE file for details.
