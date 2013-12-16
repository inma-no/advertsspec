# JavaScript animations are forbidden before an user interaction

Making the initial rendering as fast as possible is essential and therefor using JavaScript animations (ex. jQuery.animate or call to setTimeout) are forbidden before an user interactions (ex. swipe or touch). 

What you can do is simple JavaScript initialization such as simple resizing of banner content or similar operations. However, keep in mind that some calls to the DOM API causes the entire banner to repaint. 