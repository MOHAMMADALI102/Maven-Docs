# How do I add a Size Chart to my products?

MAVEN comes with the ability to display a sizing guide for your products:

<figure><img src="https://documentation.fuelthemes.net/wp-content/uploads/sites/2/2023/03/image-3-1024x611.png" alt=""><figcaption></figcaption></figure>

This can be set up inside the **Variant Picker** block inside your Product Information section:

<figure><img src="https://documentation.fuelthemes.net/wp-content/uploads/sites/2/2023/03/image-4.png" alt="" width="563"><figcaption><p>Add your Sizing guide variant name to display the sizing guide link.</p></figcaption></figure>

You need to add a Sizing Guide label and select a page to be displayed inside the lightbox.

### I cannot see the Sizing guide link

This is probably because of your **Variant name**. Please make sure that you have added it correctly.

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-21 16.png" alt=""><figcaption><p>Variant name is called “Size”</p></figcaption></figure>

However, this can be edited inside **sections/main-product.liquid** file. Please find the below code:

```
{% raw %}
{%- if option_slug == sizing_guide_variant -%}
{% endraw %}
```

and replace “sizing\_guide\_variant” with your variant slug.
