# JavaScript animations are forbidden before an user interaction

It is important to note that _after_ an user interaction there are no restrictions as to what you can do with JS animations. However, there are some things that should be taken into considerations when choosing how to do animations

Making the initial rendering as fast as possible is essential to having successful campaigns and therefor using JavaScript animations (ex. jQuery.animate or call to setTimeout) are forbidden before an user interactions (ex. swipe or touch). 

What you can do is simple JavaScript initialization such as simple resizing of banner content or similar operations. However, keep in mind that some calls to the DOM API causes the entire banner to repaint. 


# Why is it forbidden to use JS animations before an interaction?

There are numerous JS libraries available that do a great job of animating content. The footprint is small and they can do the job even on mobile, so how come we can't use them? However in a multi-device world there are some things we need to take into consideration when it comes to using JS for animations.

### Scrolling

Browsers render a page on a single thread, so if multiple banners use JavaScript animations at the same time as the host page use JavaScript for scrolling, the browser will have to finish browser-internal stuff, plus scrolling, plus the JavaScript animation-code for each banner within the 16.67 ms timeframe to get 60 fps scrolling. For CSS animations the browser can do many optimizations and run the animation logic with native code. It's very hard to get scrolling to perform well even without any banners. So if banners only use a tiny bit of extra CPU the scrolling might become yanky.

### WebViews in native apps

Content is widely viewed in WebViews and means an even less performant environment than the regular web browsers. One important aspect when it comes to JS animations is that in WebViews all animations done in CSS are performed by the GPU, wereas the JS animations are performed on the CPU. This makes for a drastic difference in performance and battery life on mobile devices.




