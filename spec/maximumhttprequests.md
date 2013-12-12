# Maximum of two HTTP requests to JavaScript libraries (one local and on external)

Purpose of this rule is to make the first time rendering as fast as possible.

When using commonly used libraries you should use a CDN. It increases the chance of the library already being cached by the user. [Googles CDN service](https://developers.google.com/speed/libraries/devguide#jquery) is one good options for choosing a CDN.

You can download JavaScript asynchronously after the page is rendered.

# Minify your JavaScript
You should minify and concatenate your JavaScript in order to prevent unnecessary HTTP requests. 

Here is a list of available online resources:
* [JSCompress](http://jscompress.com/)
* [JS Beautifier](http://jsbeautifier.org/)
* [Uglify]()
* [YUI Compressor](http://yui.github.io/yuicompressor/)