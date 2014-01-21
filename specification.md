# Specifications for the Inline format - FINN.no

This is the specifications for both the HTML banners and image banners. Inline is an advertising format used across all devices (mobile, tablet and desktop). As for now, HTML is recommended as it will be fully responsive across all screens. 

For advertisers and agencies using AdForm, use [AdForms specifications](http://test.adform.com/banners/Specifications/finn/index.htm) under the headline Responsive HTML5. 

## 1. Dimensions

### Height and width
* Banner: always 100% width of the page, but has fixed height.
* Box: a square where the width and height always are equal but the dimensions varies.

### Size
* Max 100 kb in compressed state (all files compressed/zipped together).
* You can use JavaScript libraries like jQuery from [Googles CDN service](https://developers.google.com/speed/libraries/devguide#jquery) without its size counting against the total size of the ad.
* Resources loaded after a user interaction does not count against the total size of the ad.

Note: The size limitation is on the initial load. You can lazy load additional content, but for the first rendering this is the limit.

## 2. Limitations
* Viewport can't be set to device width in the ad

		<meta name="viewport" content="width=devicewidth">

* You can not use the [Geo Location APIs](spec/geoapi.md)
* The HTML-file should just be one file with all CSS required for the ad inline in the HTML.
* [Maximum of two HTTP requests to JavaScript libraries (one local and on external).](spec/maximumhttprequests.md)

* Animation which _before an user interaction_ must be [written in CSS](spec/cssforanimations.md)
 * [JavaScript animations](spec/jsanimations.md) are forbidden before an user interaction.
 * You can not use of _requestAnimationFrame_ as it break features in the host document.

## 3. Click counter
You must use the following method when [adding click tags](spec/clicktag.md) to the ad:

	<div id="Banner" data-responsive="225h" onclick="window.open('http://www.url.no','new_window');">

Or alternativly you can add an event listener using JavaScript.

## 4. Default styling of Banner

CSS rules can only be set to classes or IDs. You can not set rules directly to elements like span or div.

The div element should only have the following styling:

    display: block; /* browser default */
    position: static; /* browser default */
    width: 100%;
    height: 225px;
    cursor: pointer;

Additional styling must be done on a new div/element within that container (ex Banner in the sample below).

    <div id="Banner" data-responsive="225h" 
    	onclick="window.open('http://www.url.no','new_window');" 
    	style="display:block;width:100%;height: 225px;">
        <div style="position:relative;"></div>
    </div>  

Read additional [styling tips](stylingingtips.md).

## 5. Third party code
* Must be sent as JavaScript code

## 6. Older formats
Many ads today is only a single image adapted i height/width to different formats (mobile and tablet).

As of 26th of August the image banners(PNG/JPEG/GIF) will be produced to fill the whole width and height in portrait,
while they will be centered in landscape without scaling. The format size is based on iPhone and iPad.

* Mobile: 310*225 maks 50 kb
* Tablet + Desktop: 758*225 maks 100 kb

