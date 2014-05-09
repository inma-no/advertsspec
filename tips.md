# What should I focus on learning?

* CSS animations/transitions/transforms
* Web Performance
* Browser support & vendor prefixes
* NodeJS toolchain
* The JavaScript DOM-api (instead of jQuery)


# Tips for improved performance

* Keep the number of HTTP requests to a minimum
* Compress images as much as possible without visible image noise. [PNG](http://youtu.be/cqNTCf6oCJ8) VS [JPEG](http://youtu.be/w655JPmzpUI). With tools such as [Tinypng](https://tinypng.com/)
* On the initial load only use JavaScript to add event listeners
* Load the scripts last, so text and images show up while scripts are loading
* For smooth CSS-animations, [only animate position, scale, rotaion and opacity](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/)
* [How Browsers Work](http://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)

# What about Web Fonts?

When using Web Fonts keep in mind that users might not download the font because of bandwith issues, so make sure the fallback looks good. Design a version which looks good with the fallback version, then make sure the Web Font version also looks good.


# What about new APIs and features in browsers?

Technology such as WebGL or new options in CSS can be used, but you must make sure that it has a built in fallback for mobile and legacy browsers.

# How do I make animations work in Internet Explorer <= 9?

You can use IE conditional comments to load JavaScript only in IE

    <!--[if lte IE 9]>
      <script src="ie-fallback.js"></script>
    <![endif]-->

# Useful resources
* [HTML5 rocks](http://www.html5rocks.com/) for lots of articles about HTML5 (by Google)
* [Can I use...](http://caniuse.com/) for browser support
* [Smashing Magazine: The Guide To CSS Animation](http://coding.smashingmagazine.com/2011/09/14/the-guide-to-css-animation-principles-and-examples/)
* Book: [High Performance Web Sites](http://shop.oreilly.com/product/9780596529307.do)
* Book: [Even Faster Web Sites](http://shop.oreilly.com/product/9780596522315.do)
* Book: [High Performance Browser Networking](http://shop.oreilly.com/product/0636920028048.do)
* Book: [JavaScript: The Good Parts](http://shop.oreilly.com/product/9780596517748.do)

# Tools
* Most of the following examples are Node-based tools. If you haven't used Node before, go to [http://nodejs.org/](http://nodejs.org/) and get started. Most likely it will change your life. Also, if you prefer tools such as Grunt, Gulp or other, many of the tools below have an associated plugin.*
* [Image-min](https://github.com/kevva/image-min) to minify images.
* [Html-minifier](https://github.com/kangax/html-minifier) to minify HTML.
* [Clean-css](https://github.com/GoalSmashers/clean-css) to minify CSS.
* [UglifyJS](http://lisperator.net/uglifyjs/) to minify Javascript.

Validate your banner using [Page Speed Insights](https://chrome.google.com/webstore/detail/pagespeed-insights-by-goo/gplegfbjlmmehdoakndmohflojccocli). This Chrome plugin analyses your page and gives you greate improvement suggestions.


Obviously. [devtools.chrome.com](https://developers.google.com/chrome-developer-tools/). #networkTab #emulation #timeline

#Accessibility

Making content accessible to everyone is encouraged. Good accessibility can help people with disabilities (e.g. blindness and low vision, hearing loss, learning disabilities and limited movement) perceive content in a meaningful way.

* [Web Content Accessibility Guidelines (WCAG) 2.0 Overview](http://www.w3.org/WAI/intro/wcag.php)
* [Accessible Rich Internet Applications (WAI-ARIA) Overview](http://www.w3.org/WAI/intro/aria)
