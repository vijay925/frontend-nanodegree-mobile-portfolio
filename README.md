#### Part 1: Optimize PageSpeed Insights score for index.html

Here is how I optimized the rendering path:

1. Minified HTML, CSS, JS
2. Compressed Images
3. Deferred JS using defer and async attributes
4. Inlined style.css and deferred print.css using `media` attribute

#### Part 2: Optimize Frames per Second in pizza.html

I used chrome dev tools to analyze the timeline of the JS execution. I noticed that a few of the functions were doing redundant work and causing constant reevaluation of the styles within a loop. I tried to factor out code that didn’t need to be in the loop and also minimized accessing of DOM objects. It significantly improved the performance and brought the average fps to 60.