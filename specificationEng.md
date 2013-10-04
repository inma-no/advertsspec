## Physical Size
* Height: 225px
* Width: 100%
* Size:
	- Max 100 kb in compressed state (all files compressed/zipped together).
	- You can use the jQuery library without counting its size in total size of the banner ad if you use the latest minified version from [Googles CDN service](https://developers.google.com/speed/libraries/devguide#jquery) (ex- [jQuery 2.0.0](http://ajax.googleapis.com/ajax/libs/jquery/2.0.0/jquery.min.js))

## Limitations
* Viewport can't be set to device width in the ad

		<meta name="viewport" content="width=devicewidth">

* You can not use the Geo Location APIs
* The HTML-file should just be one file with all CSS required for the ad inline in the HTML.
* Maximum of two HTTP requests to JavaScript libraries (one local and on external).
* Animation which before an user interaction must be written in CSS. For tutorial and examples on CSS animations, check [Using CSS animations](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_animations)
 * JavaScript animations (ex. jQuery.animate or call to setTimeout) are forbidden before an user interactions (ex. swipe or touch).
 * You can not use of _requestAnimationFrame_ as it break features in the host document.
* References to resources must start with http:// or https:// , not only //. Because of limitations in our delivery system.

## Click counter:
You must use the following method when adding clicks to the ad:

	<div id="Banner" data-responsive="225h" onclick="window.open('http://www.url.no','new_window');">

## Default styling of Banner

CSS rules can only be set to classes or IDs. You can not set rules directly to elements like span or div.

The div element should only have the following styling:

    display: block; /* browser default */
    position: static; /* browser default */
    width: 100%;
    height: 225px;

Additional styling must be done on a new div/element within that container (ex Banner in the sample below).

    <div id="Banner" data-responsive="225h" onclick="window.open('http://www.url.no','new_window');" style="display:block;width:100%;height: 225px;">
        <div style="position:relative;"></div>
    </div>  

# Third party code
* Must be sent as JavaScript code

## Use of older formats
Many ads today is only a single image adapted i height/width to different formats (mobile and tablet).

As of 26th of August the image banners(PNG/JPEG/GIF) will be produced to fill the whole width and height in portrait,
while they will be centered in landscape without scaling. The format size is based on iPhone and iPad.
* Mobile: 310*225 maks 50 kb
* Tablet: 758*225 maks 100 kb
