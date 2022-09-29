# Browser Rendering

## What is browser rendering ?
Rendering is a process used in web development that turns website code into the interactive pages users see when they visit a website. The term generally refers to the use of HTML, CSS, and JavaScript codes. The process is completed by a rendering engine, the software used by a web browser to render a web page. Because of its close association with web browsers, rendering engines are commonly referred to as browser engines.

Whenever you are developing a website, there are certain things that are very essential for a good user experience. Some of the common problems a website may encounter could be slow loading of the resources, waiting for unnecessary files to download on initial render, a flash of unstyled content (FOUC), etc. To avoid such problems, we need to understand the lifecycle of how a browser renders a typical webpage.

## we need to know what is DOM
When the browser reads HTML code, whenever it encounters an HTML element like html, body, div etc., it creates a JavaScript object called a Node. Eventually, all HTML elements will be converted to JavaScript objects.

_Since every HTML element has different properties, the Node object will be created from different classes (constructor functions). For example the Node object for the div element is created from HTMLDivElement which inherits Node class. For our earlier HTML document, we can visualize these nodes using a simple test as below._

***After the browser created Nodes from the HTML document, it has to create a tree like structure of these node objects. Since these HTML elements in the HTML file are nested inside each other, the browser needs to replicate that but using Node Objects it has previously created. This will help the browser effeciently render and manage the webpages throughout its lifecycle.***


<h align="center">
  <img src="https://www.guru99.com/images/JavaScript/javascript8_1.png" />
</h>


```
A DOM tree for our HTML document looks like above. A DOM tree starts from the topmost element in HTML element and branches out as per the occurrence and nesting of HTML elements in the document. Whwnever HTML elements is found, it creates a DOM node object from its respective class
```
## CSS Object Model (CSSOM)

When we design a website, our intentions are to make it as good looking as possible. And we do that by providing some styles to HTML elements.In the HTML page, we provide stypes to HTML elements using [CSS](https://gist.githubusercontent.com/thatisuday/712a3fd1301ff31a316b9e59c69723f9/raw/dd005e164f8368e2f5bae778dc0ae802a013ed87/styles.css)(Cascading style sheets)

## Rendering Sequence

When a web page is loaded, the browser first reads the HTML text and constructs DOM Tree from it. Then it processes the CSS whether that is inline, embedded, or external CSS and constructs the CSSOM Tree from it. After these trees are constructed, then it constructs the Render-Tree from it. Once the Render-Tree is constructed, then the browser starts the printing individual elements on the screen.

## Importance of Rendering

* Webpage rendering affects how a page is indexed by bots and experienced by users.
* Understanding the impact of rendering on search engine rankings and SEO (Search Engine Optimisation) results should be a key consideration for any web development team.
* Many websites, building a website primarily in JavaScript may provide the most user-friendly interface

## References
1. [Implement Dynamic Rendering Google Search Central](https://developers.google.com/search/docs/crawling-indexing/javascript/dynamic-rendering)  Retrieved 8 December 2020.

1. [Using site speed in web search ranking](https://developers.google.com/search/blog/2010/04/using-site-speed-in-web-search-ranking) Google Search Central. Retrieved 11 December 2020.
Related links

## Related links
* [https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)