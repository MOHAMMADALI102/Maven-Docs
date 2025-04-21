# How to open all external links in new window?

Shopify does not have a setting to set links to open in new tab or the current tab.

However, there is an easy solution. You can add the below code at the end of **assets/app.js** or **assets/app.min.js** depending on your theme:

```
var links = document.links;
for (let i = 0, linksLength = links.length ; i < linksLength ; i++) {
  if (links[i].hostname !== window.location.hostname) {
    links[i].target = '_blank';
    links[i].rel = 'noreferrer noopener';
  }
}
```
