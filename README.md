## [The-Scent](http://www.scent.com.sg/)

If you want to use your custom HTML page without WordPress altering it, you can still rename it to index.php but avoid using WordPress template tags. Simply include the PHP template name at the top:

```
&lt;?php
/* Template Name: CustomPage */
?&gt;
```
Then, upload this file to your theme folder. When you create a new page in WordPress, select "CustomPage" from the template dropdown. This way, WordPress will use your static HTML content as-is without modification.

---
The error indicates that your theme package is missing the style.css file, which is essential for WordPress themes. This file should include theme information and styles.

To fix this:

1. Create a style.css File: In your theme folder, add a style.css file with the following header information:

```
/*
Theme Name: Your Theme Name
Theme URI: http://example.com
Author: Your Name
Author URI: http://example.com
Description: A brief description of the theme.
Version: 1.0
*/  
```
2. Add Styles: Include any CSS styles you want for your theme below the header.

3. Repack and Upload: Zip the theme folder again and upload it through the WordPress theme installer.

This should resolve the installation issue.

---
Yes, you can create an empty style.css file with just the required header information. This file is mandatory for WordPress to recognize and install your theme, even if you don't need it for styling purposes. Just ensure the header is correctly formatted as shown:

```
/*
Theme Name: Your Theme Name
Theme URI: http://example.com
Author: Your Name
Author URI: http://example.com
Description: A brief description of the theme.
Version: 1.0
*/  
```
This will allow your custom theme to be installed without any issues.

---
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
