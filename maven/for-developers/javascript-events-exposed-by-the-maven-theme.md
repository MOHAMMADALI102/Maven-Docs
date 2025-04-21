# JavaScript events exposed by the MAVEN theme

We build our themes with developers in mind. To allow you to easily extend the theme without modifying the internals or to be notified when something happens in the theme, several events are triggered in JavaScript.

### The following **exposed events** are available to use as a blueprint to get started:

#### Item added to cart

This event fires when an item is added to the cart. The Cart Drawer must be enabled for this event to be exposed. The product object is passed within the detail object.

```javascript
document.addEventListener("cart:item-added", function (evt) {
    console.log("Cart item added");
    console.log(evt.detail.product);
});
```

#### Product variant change

This event fires when a variant product is selected. A Variant selector block must be enabled on the product template or featured product section for the event to be exposed. The selected variant object is passed within the detail object.

```javascript
document.addEventListener("product:variant-change", function (evt) {
    console.log("Product variant changed");
    console.log(evt.detail.variant);
});
```

#### Product Quick View drawer opened

This event fires when a product is viewed inside Quick View. Product handle and product URL is passed within the detail object.

```javascript
document.addEventListener("quick-view:open", function (evt) {
    console.log("Quick view opened");
    console.log(evt.detail.productHandle);
    console.log(evt.detail.productUrl);
});
```

#### Search Drawer opened

This event fires when the search drawer is opened.

```javascript
document.addEventListener("search:open", function (evt) {
    console.log("Search drawer opened");
});
```

#### Cart Drawer opened

This event fires when the cart drawer is opened.

```javascript
document.addEventListener("cart-drawer:open", function (evt) {
    console.log("Cart drawer opened");
});
```

#### Line item changed

There are two events, one triggers before the cart contents are changed, and the other when new cart contents are rendered.

```javascript
document.addEventListener("line-item:change:start", function (evt) {
    console.log("Line item changed");
    console.log(evt.detail.quantity);
});
document.addEventListener("line-item:change:end", function (evt) {
    console.log("Line item changed");
    console.log(evt.detail.quantity);
    console.log(evt.detail.cart);
});
```

#### Pagination, next page loaded

When **click to load** or **infinite** pagination type is selected and new page is loaded via AJAX:

```javascript
document.addEventListener("pagination:page-changed", function (evt) {
    console.log("Pagination: new page loaded");
    console.log(evt.detail.url);
});
```

#### Refresh cart content

If you are using a 3rd party app and it has modified the cart or its content, you can refresh the theme UI by running the below snippet:

```javascript
document.documentElement.dispatchEvent(new CustomEvent('cart:refresh', {
  bubbles: true
}));
```

```
This will ONLY update the UI. This will not, for instance, automatically open the side cart. To do that, you will need to open it manually in JavaScript.
```
