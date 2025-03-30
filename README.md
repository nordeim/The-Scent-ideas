## [The-Scent](http://www.scent.com.sg/)

# Creating a Custom Page Using an HTML File in WordPress

To create a custom page using an HTML file in WordPress, follow these steps:

## 1. Create a Template File

Open a text editor and save your HTML content as a PHP file, for example, `custompage.php`. Ensure it includes a template name at the top like this:

```php
<?php
/* Template Name: CustomPage */
?>
```

## 2. Upload the Template File

Use an FTP client (like FileZilla) to upload this file to your theme's directory, usually located at:

```
wp-content/themes/your-theme-name/
```

## 3. Assign the Template to a Page

In WordPress, create a new page or edit an existing one, and in the **Page Attributes** section, select your custom template from the **Template** dropdown menu.

For more detailed steps, you can check the guide on creating WordPress themes.

---
