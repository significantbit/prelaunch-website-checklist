# Pre-launch Website Checklist
A checklist for web projects that needs to be gone through before release.

1. Language
1. Metadata
    1. Opengraph
1. Favicons
1. Accessibility
1. Error pages
1. Cookies
1. Markup Validation
1. Tracking codes (Google Analytics, Facebook Pixels etc)
1. Performance
1. SSL/HTTPS
1. Security headers
1. Robots.txt
1. Documentation

## Audit tools
**General**

[webdevchecklist.com](https://webdevchecklist.com), [web.dev/measure](https://web.dev/measure/)

**Accessibility**

[WAVE Evaluation Tool (Chrome Extension)](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)

**Performance**

[PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/), [webpagetest.org](http://www.webpagetest.org/), [web.dev/measure](https://web.dev/measure/)

**Security**

[securityheaders.com](https://securityheaders.com/)

**Open graph/sharing**

[Facebook sharing debugger](https://developers.facebook.com/tools/debug/), [Open Graph Preview (Chrome Extension)](https://chrome.google.com/webstore/detail/open-graph-preview/ehaigphokkgebnmdiicabhjhddkaekgh)

**Tracking/Analytics**

[Facebook Pixel Helper (Chrome Extension)](https://developers.facebook.com/docs/facebook-pixel/support/pixel-helper)

---

## 1. Language

The `<html>` element at the top of your document should have the language specified. Remember about proper language codes: `en-US`, `sv-SE`, etc.

Example: `<html lang="sv-SE">`


## 2. Metadata

The site needs those in the `<head>`:

- `<title>` - the page title, every subpage has it's own (with the format `Page - (- Category) - Site name`)
- `<meta name="description">` - a short paragraph (max 160 char) describing the content of main site, category or a single post
- `<link rel="home" href="http://site.url">` - a link to home root page
- `<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">` - [Don't disable zoom](http://adrianroselli.com/2015/10/dont-disable-zoom.html)

Optional and ocassionaly beneficial tags:

- `<meta name="keywords">` - a list of `, `-separated tags that describes the content
- `<meta name="author">` - a list of `, `-separated names of main people involved in the project


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
- [Open Graph Preview (Chrome Extension)](https://chrome.google.com/webstore/detail/open-graph-preview/ehaigphokkgebnmdiicabhjhddkaekgh)


## 3. Favicons

Use Favicons. A great tool for this is http://realfavicongenerator.net.


## 4. Accessibility

Resources:
- [WCAG 2.1](https://www.w3.org/TR/WCAG21/)
- [web.dev/measure](https://web.dev/measure/)
- [WAVE Evaluation Tool (Chrome Extension)](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)


## 5. Error pages (404, 500)

Include pages for error pages such as 404 and 500. Make sure the styling is similar to the main site and give a brief description about what might have went wrong.

Also use an error/exception reporting service, like Honeybadger.


## 6. Cookies

We need to inform visitors if the site uses cookies.


## 7. Markup Validation

Make sure to fix all invalid markup.

Resources:
- https://validator.w3.org/
- https://validator.nu/


## 8. Tracking codes (Google Analytics, Facebook Pixels etc)

Set up all appropriate tracking codes.

Resources:
- [Facebook Pixel Helper (Chrome Extension)](https://developers.facebook.com/docs/facebook-pixel/support/pixel-helper)


## 9. Performance

Make sure the site has good performance.

Resources:
- [PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/)
- [Web Page Performance Test](http://www.webpagetest.org/)
- [web.dev/measure](https://web.dev/measure/)

## 10. SSL/HTTPS

All sites should be protected with HTTPS, even ones that don't handle sensitive data. HTTPS prevents intruders from tampering with or passively listening in on the communications between your app and your users, and is a prerequisite for HTTP/2 and many new web platform APIs. 

## 11. Security headers

Deploy security response headers. Security headers audit can be done at [securityheaders.com](https://securityheaders.com/).

## 12. Robots.txt

Add a robots.txt file to inform search engine spiders how to interact with indexing your content.

## 13. Documentation

A `README.md` with the page maintenance, installation instructions and inner workings explained. However, don't be too specific. Your HTML markup, SCSS styles and JavaScript should be semantic and well commented on its own.
