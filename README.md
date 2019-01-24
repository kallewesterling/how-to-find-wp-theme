# How to find the WordPress theme behind a specific website

I recently encountered a question about whether there is a plugin or a web service that can detect WordPress themes behind specific websites. There's no need for it, since all the code is available right on the site and we can easily track it down in a few simple steps.

## Step 1: Navigate to the website

First, you find the WordPress-created website that you want to investigate. In this case, I'll just my personal website.

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-01.png" width="50%" />

## Step 2: Find the source code for the website

Second, you have to find the source code (HTML) for the website. It is easily done but the method depends on the browser.

_If you are using Google Chrome, you'll find the menu choice under `View > Developer > View Source`._

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-02.png" width="50%" />

_If you are using Mozilla Firefox, you'll find the menu choice under `Tools > Web Developer > Page Source`._

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-03.png" width="50%" />

_If your browser isn't listed here, just navigate to Google's search engine and ask for how your browser can reveal the HTML code of a website to you._

## Step 3: Search for the CSS stylesheet(s) of the website

Third, press `Command + F` on your keyboard to search the code for `style.css`. The `style.css` file is a CSS-file containing all the stylings of your website. That is at least 50% of what a "theme" in WordPress is: a way of styling pre-existing, "unstyled" HTML.

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-04.png" width="50%" />

You should be able to find one or two occurrences of `style.css` in your code. If you only find one, it means that the website only uses _one theme_. It hasn't been amended or re-styled using what's called a "child theme." If you find two, it means that the website uses a child theme.

Pro-tip: You can [read more about child and parent themes on the WordPress developer pages](https://developer.wordpress.org/themes/advanced-topics/child-themes/) but suffice here to say that the definition of a child theme is that it "inherits the look and feel of the parent theme and all of its functions, but can be used to make modifications to any part of the theme. In this way, customizations are kept separate from the parent theme’s files. Using a child theme lets you upgrade the parent theme without affecting the customizations you’ve made to your site."

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-05.png" width="100%" />

## Step 4: Investigate the CSS file(s)

Fourth, open the CSS-file (or both the CSS-files if you found two) by clicking their names in the source code. A great tip is to hold the `Command` key on your keyboard when you press the links. That way, the links are opened in new tabs in your browser window.

_(The hyperlinks are blue in the past screenshot and should be clickable; if they're not you can always copy and paste the link to each CSS file into your browser window and navigate to them that way.)_

Once you have the CSS-files for the theme open, you can read about who made the theme: in this case, Anders Noren's excellent [Fukusawa](https://www.andersnoren.se/teman/fukasawa-wordpress-theme/) was used. (In our case here, you can also see that the child theme was made by yours truly.)

The `Theme-URI` (if it is noted in your CSS file) can tell you more about the theme. Just copy and paste the link into your browser window to read more about which theme it is.

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-06.png" width="100%" />

<img src="https://github.com/kallewesterling/how-to-find-wp-theme/blob/master/screen-07.png" width="50%" />
