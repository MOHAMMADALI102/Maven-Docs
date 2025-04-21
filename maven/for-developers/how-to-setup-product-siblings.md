# How to setup Product Siblings?

**Product Siblings** is the ability to link directly to other products as product swatches. The result is a rich product detail page that includes swatches with images that represent each variant option.

When you view a siblings product, only the images associated with that variant option, plus product details, and prices for the variant are shown:

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-21 112030.png" alt=""><figcaption><p>Product siblings shown similar to Color variants.</p></figcaption></figure>

### Setup Steps:

There are five main components to setting up product siblings:

1. Creating individual products. Each product can have variants like sizes.
2. Group the sibling products into a collection. This collection does not have to be displayed on your storefront.
3. Define two custom metafields to link each product together which will automatically create linked product swatches.
4. Update the metafield information for each product.
5. Add the Siblings block to the Product template in the Theme Editor.

#### Create individual products

Each sibling is an individual product. Using custom metafields, the theme will connect these products together and auto-generate the swatch images using their preview images or swatch options inside theme settings.

Example of individual products in product admin:

<figure><img src="../../.gitbook/assets/Untitled design1.png" alt=""><figcaption><p>Separate products.</p></figcaption></figure>

> In this example, we will combine all these products into one product using the Siblings feature.\
> Therefore, each product is a duplicate of the other with the exception of the color in the title and the product images.\
> Each product represents one color for the combined product.

#### Create a collection containing siblings

After creating the products, place them all in one collection. **The collection needs to be published on the Online Store:**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 175247.png" alt=""><figcaption></figcaption></figure>

#### Create a Metafield for Sibling Collection

Use the metafields editor under **Settings** in the **Shopify Admin > Settings > Custom Data > Products**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 171451.png" alt=""><figcaption></figcaption></figure>

Name your metafield **`theme.siblings`**, which will be used to select the collection. The **content type** is: **Single line text and One value.**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 172652.png" alt=""><figcaption></figcaption></figure>

> Please ensure you change the Namespace and key to **`theme.siblings`** By default, the namespace begins with **`custom`**. This will need to be changed to **`theme`**.

#### Create a Metafield for Sibling Colors

Use the metafields editor under **Settings** in the **Shopify Admin > Settings > Custom Data > Products**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 171451.png" alt=""><figcaption></figcaption></figure>

Name your metafield **`theme.sibling_color`**, which will be used to select the collection. The **content type** is: **Single line text and One value.**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 172327.png" alt=""><figcaption></figcaption></figure>

> Please ensure you change the Namespace and key to **`theme.sibling_color`** By default, the namespace begins with **`custom`**. This will need to be changed to **`theme`**.

#### Setup Sibling Products

After creating the metafields in the previous steps, we complete the setup in the Product Admin. Add the associating information to each of the newly created metafields for each product.

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 173314.png" alt=""><figcaption></figcaption></figure>

**Sibling color**

This value is to identify the swatch (color) and label-name of the swatch.

A nice advantage when using Siblings is the ability to create descriptive names for each swatch.

You’re not limited to basic color names.

**Siblings**

This metafield is used to map each product to the correct collection they belong to. Each group of products should have already been added to a collection.

For example, each product sibling for the product “Jackie T-Shirt” belongs to a collection with the handle of `sibling-jackie-t-shirt`.

#### Add Siblings block to your Product Information section.

After creating the metafields and adding values to each of your products, the final step is to add the Siblings block to your Product template under the Product information section:

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 172041.png" alt=""><figcaption><p>Add block > Siblings</p></figcaption></figure>

Select metafields inside block settings:

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 175535.png" alt=""><figcaption></figcaption></figure>

#### Changing the Color label

Product siblings by default are used to replace the color variant by grouping similar products and generating custom swatches for each color option.

If you would like to change the Siblings feature to replace to be used with other variant types instead, you can apply a global change to accommodate that.

In the above example, if your store is selling are artwork and would rather replace the **Color** label with **Styles**:

**Go to Edit Default Theme Content:**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 175600.png" alt=""><figcaption></figcaption></figure>

**Change the value under Products**. You can also search for “siblings” to find it quicker:

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-19 171209.png" alt=""><figcaption></figcaption></figure>

When changing the Siblings Label value in the default theme content, the change becomes global. The Siblings feature will always show the new value (“Style”) for any Siblings products you build on your store.

You can still use regular Swatches for other products and display “Color” as a label for those. However, any Siblings products will have the new value “Style” from our example.
