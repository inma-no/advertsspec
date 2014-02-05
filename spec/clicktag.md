# Click counter

The specification says that you must either use the _onclick_ attribute or attach an event listener to the container.
The reason you can not use the _target_ attribute, is that it would not work for advertisements viewed inside a WebView on a mobile device. 

Using the _onclick_ attribute is supported by all browsers, which is why it is recommended to use. Adding event listeners would require handling of the difference between event models in browsers.
