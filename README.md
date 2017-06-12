# Pre-launch Website Checklist
A checklist for web projects that needs to be gone through before release.

1. Language
2. Metadata
    1. Opengraph
3. Favicons
4. ARIA Landmark Roles
5. Error pages
6. Cookies
7. Markup Validation
8. Google Analytics
9. Humans
10. Futurefriendliness
11. Performance

A good resource, available as a Chrome extension: http://webdevchecklist.com/

## 1. Language

A `<html>` element at the top of your document should have the language specified. Remember about proper language codes: `en-US`, `sv-SE`, etc.

Most common example: `<html lang="sv-SE">`


## 2. Metadata

The site needs those in the `<head>`:

- `<title>` - the page title, every subpage has it's own (with the format `Page - (- Category) - Site name`)
- `<meta name="description">` - a short paragraph (max 160 char) describing the content of main site, category or a single post
- `<link rel="home" href="http://site.url">` - a link to home root page
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` - [Don't disable zoom](http://adrianroselli.com/2015/10/dont-disable-zoom.html)

Optional and ocassionaly beneficial tags:

- `<meta name="keywords">` - a list of `, `-separated tags that describes the content
- `<meta name="author">` - a list of `, `-separated names of main people involved in the project
- `<link rel="author" href="humans.txt">` - an url leading to the `humans.txt` file


### 2.1. Opengraph

Opengraph meta elements -- mainly for social media link sharing:

- `<meta property="og:type" content="website">` - the type of document, for the most projects it's "website"
- `<meta property="og:site_name" content="name">` - the name of the site, `Significant Bit`
- `<meta property="og:title" content="title">` - the same as in `<title>`
- `<meta property="og:description" content="description">` - the same as in meta description
- `<meta property="og:url" content="http://site.url">` - The page url
- `<meta property="og:image" content="social-image-1200x630.png">` - an image with dimensions 1200x630 px
- `<meta property="og:image:width" content="1200">` - Image width in pixels
- `<meta property="og:image:height" content="630">` - Image height in pixels

Documentation/resources:
- [Open graph](http://ogp.me/)
- [A Guide to Sharing for Webmasters (Facebook)](https://developers.facebook.com/docs/sharing/webmasters#media)
- [Facebook sharing debugger](https://developers.facebook.com/tools/debug/)


## 3. Favicons

Use Favicons. A great tool for this is http://realfavicongenerator.net.


## 4. ARIA Landmark Roles

- banner
- complementary
- contentinfo
- main
- navigation
- search
- form

https://accessibility.oit.ncsu.edu/using-aria-landmarks-a-demonstration/

## 5. Error pages (404, 500)

Include pages for error pages such as 404 and 500. Make sure the styling is similar to the main site and give a brief description about what might have went wrong.


## 6. Cookies

We need to inform visitors if the site uses cookies.

## 7. Markup Validation

Some markup validation could always be good, https://validator.w3.org/. 


## 8. Google Analytics

Set up a Google Analytics account on info@significantbit.se. If the projects client has its own Google Analytics, ask for an invite to theirs so we can have access to all website data through info@significantbit.se.


## 9. Humans

Introduction and being thankful in the `humans.txt` file.

http://humanstxt.org/


## 10. Futurefriendliness

A `README.md` with the page maintenace, update and inner workings explained. If the project is going to be setup by a not-so-technical colleague (like a designer, hehe) a brief "how to install/run" would be great. 

However, don't be very specific -- your HTML markup, SCSS styles and JavaScript scripts should be semantic and well commented instead.


## 11. Performance

1. Run some overall tests:
- [PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/)
- [Web Page Performance Test](http://www.webpagetest.org/)
2. Optimize images with [TinyPNG](https://tinypng.com/) or similar 
3. Check accessibility at tiny screens
4. Check links and interactive elements for `fat-fingers`
