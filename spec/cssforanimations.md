# Animation which before an user interaction must be written in CSS

The purpose is to make animations as nice as possible for the end user. CSS animations gets rendered by the GPU, which greatly outperforms animations done in JavaScript. 

For tutorial and examples on CSS animations, check [Using CSS animations](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_animations)

## Dealing with legacy web browsers

Browsers which doesn't support CSS animations must be dealt with. The best solution is to provide an image fallback campaing. 
Another solution is to code the banner with using the progressive enhancement tecnique. 