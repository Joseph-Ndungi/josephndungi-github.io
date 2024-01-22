# Web Performance - Key metrics to ensure your website is Performant

## Web performance is all about making websites fast, including making slow processes seem fast

In essence, web performance is about both the measurable aspects and the user's perceived experience when interacting with a site or app

### Key areas include

1. **Reducing Load Time**: This involves minimizing the size and number of files needed to render a website, and using techniques like preloading to speed up the process.

2. **Usability from the Start**: We focus on loading website assets efficiently, enabling users to start interacting with the site quickly. Techniques like lazy loading enhance this experience.

3. **Smoothness and Interactivity**: A seamless user experience is crucial. We explore best practices in creating smooth animations and responsive interfaces.

4. **Perceived Performance**: It's not just about how fast a website loads, but how fast it feels to the user. Strategies like engaging loading screens can significantly improve user perception.

5. **Performance Measurements**: We delve into various metrics and tools for measuring and optimizing web performance, ensuring that the site not only performs well but continues to do so over time.

Maintaining optimal performance is relatively straightforward for basic websites. However, the task becomes more challenging with intricate web applications, where delivering a consistently smooth user experience is crucial.

The problem that exists is that while our website may behave as expected on our devices, our users won’t be accessing the device from our devices, but their own and under different circumstances.

<!-- ![It works on my machine](https://hackernoon.imgix.net/hn-images/1*ookfwogTLx_1qhHaiFJoJw.png "Your machine isn’t the real world") -->


<img src="https://hackernoon.imgix.net/hn-images/1*ookfwogTLx_1qhHaiFJoJw.png" alt="It works on my machine" title="Your machine isn’t the real world" width="100%" height="100%" />


 In light of this, I have put together a selection of key metrics that are essential for evaluating the performance of websites

#### 1. First Contentful Paint (FCP)

This performance metric, known as First Contentful Paint (FCP), gauges the time taken for the initial piece of content on a website - be it text, images, or other elements - to appear on the user's screen.

FCP measures how long it takes the browser to render the first piece of DOM content after a user navigates to your page. Images, non-white <canvas> elements, and SVGs on your page are considered DOM content; anything inside an iframe isn't included.

FCP plays a significant role in shaping a user's perception of the page's loading speed, making its optimization vital.

It's important to aim for an FCP of 2.5 seconds or less for client websites to ensure optimal performance.

When you measure LCP either using Lighthouse or PageSpeed Insight, it usually provides a list of reasons why your LCP was given a certain score and how you can optimize for it.
**Some of the common things you can do to optimize for LCP.**
***Optimize Server Response Time***

To speed up your website, use a Content Delivery Network (CDN) for your images, CSS, JavaScript, HTML, and static files. This helps with caching and improves a metric known as Time To First Byte (TTFB), which is the time it takes to receive the first byte of data from the server. TTFB affects key performance metrics like Largest Contentful Paint (LCP) and First Contentful Paint (FCP).

***Enhance Resource Discovery***
Load critical resources affecting LCP as soon as possible. Browsers have a preload scanner that prefetches items like images and stylesheets marked with `rel=preload`. Ensure your images' URLs are in the `srcset` or `src` attributes, and preload CSS background images and fonts.

***Prioritize Key Resources***
Ensure important resources load first. Use the `fetchpriority="high"` attribute for essential images. De-prioritize less critical resources to conserve bandwidth.

***Other Optimizations***

- Switch to modern image formats like WebP, ideally using an image CDN for format compatibility.
- Implement responsive images to suit different screen sizes.
- Compress images to reduce size without losing quality.
- Set appropriate cache settings to minimize repeat load times.
- Eliminate unnecessary CSS and JavaScript.
- Optimize font sizes for efficiency.

#### 2. First Meaningful Paint (FMP)
