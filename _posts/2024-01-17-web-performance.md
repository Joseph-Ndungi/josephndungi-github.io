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

![It works on my machine](https://hackernoon.imgix.net/hn-images/1*ookfwogTLx_1qhHaiFJoJw.png "Your machine isn’t the real world")

 In light of this, I have put together a selection of key metrics that are essential for evaluating the performance of websites

#### 1. First Contentful Paint (FCP)

This performance metric, known as First Contentful Paint (FCP), gauges the time taken for the initial piece of content on a website - be it text, images, or other elements - to appear on the user's screen.

FCP measures how long it takes the browser to render the first piece of DOM content after a user navigates to your page. Images, non-white canvas elements, and SVGs on your page are considered DOM content; anything inside an iframe isn't included.

FCP plays a significant role in shaping a user's perception of the page's loading speed, making its optimization vital.

It's important to aim for an FCP of 1.8 seconds or less for client websites to ensure optimal performance.

#### 2. First Meaningful Paint (FMP)

Sounds pretty similar to First Contentful Paint (FCP), right? There’s a key difference.

As the name suggests, FMP is how long it takes for the first meaningful content to display (i.e., whatever users actually want to view).

This value is often the same as First Contentful Paint (FCP) but varies based on your client’s website.


