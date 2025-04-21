# How to remove Shopify / developer footer credits

In this article, we will go through a quick tutorial for removing the Shopify / developer credits from the footer of your theme.

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-21 151147.png" alt=""><figcaption><p>Example MAVEN &#x26; Shopify credits inside the footer.</p></figcaption></figure>

### Step 1

From your **Shopify Admin** go to **Online Store** > **Themes** > click the **Actions** dropdown menu next to the theme you want to edit and click > **Edit Code**

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-21 150041.png" alt=""><figcaption></figcaption></figure>

### Step 2

In the folders navigate to **Sections** > **footer.liquid** and look / search for the following code:

```
{{ powered_by_link }}
```

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-21 151800.png" alt=""><figcaption><p>Removing the copyright text and Powered by Shopify link.</p></figcaption></figure>
