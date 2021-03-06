# MENTAL NOTE: THIS REPOSITORY HAS BEEN SPLIT INTO 3
I have decided that the former **n8iv** API would function better as 3 separate libraries:

1. [m8.js](/constantology/m8): what used to be n8iv._, will now serve as a base for most of my libraries, to eliminate duplicate utility methods
2. [id8.js](/constantology/id8): this is the old n8iv.Oo; and
3. n8iv.js: this is the old n8iv.Fn, which is this repository... right... here...

Apologies for any inconvenience caused.

# n8iv.js
n8iv is a functional programming library – for modern javascript engines – which correctly extends JavaScript Natives. Giving you a – relatively – safe and easy to use API, to make your code more succinct and efficient.

n8iv is based on the awesomeness of [prototypejs](https://github.com/savetheclocktower/prototype).

If you like the idea of having one global variable with a bunch of static functions – in no particular order – attached to it, then this is probably not the framework for you.

If you think that extending JavaScript Natives is a "bad part" of JavaScript, then this is probably not the framework for you.

If, however, you like your methods bound to your types, then come on in and sit a spell!

**n8iv will not overwrite any implementations – native or otherwise – of any methods, properties or accessors already defined.**

## WARNING!!!
While **n8iv** has been tested, the testing framework I've written and used is very much a work in progress.

Also I'm currently between virtual machine software and operating system licenses, so I have only tested on mac osx lion and snow leopard: nodejs – >= v0.6.13 – as well as current – and beta/ nightly – versions of Chrome, Safari/ Webkit and FireFox.

## Dependencies

n8iv.js only has one dependency [m8.js](/constantology/m8).

**NOTE:**
If you are using n8iv within a commonjs module, you don't need to require m8 before requiring n8iv as this is done internally and a reference to **m8** is available as: `n8iv.m8`.

```javascript

   var n8iv = require( 'n8iv' ),
       m8  = n8iv.m8; // <= reference to m8

// if running in a sandboxed environment remember to:
   m8.x( Object, Array, Boolean, Function, String ); // and/ or any other Types that require extending.
// alternatively, this does the same and returns the n8iv global
   n8iv( Object, Array, Boolean, Function, String );

```

See [m8: Extending into the future](/constantology/m8) for more information on working with sandboxed modules.

## File size

<table border="0" cellpadding="0" cellspacing="0" width="100%">
	<tbody>
		<tr><td style="width : 80px ;">n8iv.js</td><td style="width : 48px ;">4.1kb</td><td>deflate</td>
		<tr><td>n8iv.min.js</td><td>3.1kb</td><td>uglified + deflate</td>
	</tbody>
</table>

## License

(The MIT License)

Copyright &copy; 2012 christos "constantology" constandinou http://muigui.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
