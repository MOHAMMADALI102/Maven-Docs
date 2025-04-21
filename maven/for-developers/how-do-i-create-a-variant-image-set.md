# How do I create a Variant image set?

By default, Shopify only allows you to attach one image per variant. However, in some circumstances, you may want to attach different images per variant, and automatically hide those that do not belong to the selected variant. For instance, if you have a T-Shirt available in two colors (Black and White), you may want to show 3 images for the black variant and 3 different images for the white variant.

To do that, our theme comes with a built-in solution based on image alt tags. As Shopify does not offer the ability to create group of images natively, the process is manual.

### 1) Find the group / set name:

First, you will need to figure out the name of the option that will be responsible to control the change of the image set. Most of the time, the option will be called “Color”, but it can be anything (like “Fit”, “Material”… or whatever).

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-20 150357.png" alt=""><figcaption></figcaption></figure>

This option contains several colors (Blue, Orange and Pink), and the goal is to display different images when Blue is selected, different images when Orange is selected… and so on.

### 2) Edit Alt tags of the images:

Once you have found out the option name, you need to edit the ALT tag of each image. To do that, click on the image inside product’s Media gallery and click on “Edit alt text”.

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-20 150539 (1).png" alt=""><figcaption></figcaption></figure>

In the ALT tag, enter a hash character (#), followed by the option name, followed by one underscore, and the value of the option. For instance, in this example we are editing the ALT tag of an image that should appear when the “Orange” color is selected. I therefore need to enter `#color_orange`.

**If your color is made of several words** (for instance “Deep Blue”), then you must write the color name in lowercase with “-” separator between each words of the color.\
\
For instance, the correct alt tag would be: `#color_deep-blue`

> HTML Entities such as © or ® will be ignored. If your Variant name is My Great Product ®, your alt tag should be #color\_my-great-product

### 3) Repeat the process for all images.

You’ll need to tag the other images with `#color_orange` or with `#color_pink` and `#color_blue`
