# Reset user agent stylesheet (the default css from the broswer)
```css
html, body, div, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, ol, ul, li, form, fieldset, legend, label, table, header, footer, nav, section {
    margin: 0;
    padding: 0;
    border: 0;
}
```
# box-sizing

Define how the size of an element is defined:

```css
/*Main values*/
box-sizing: content-box; /*default value, content*/
box-sizing: border-box;  /*content + padding + border*/

html {
    box-sizing: border-box;
}
*, *:before, *:after {
    box-sizing: inherit;
}
```
# viewport

## Sizes
There is a difference between the real size of a device and the size in px (device-width, device-height). For example the real surface for an Iphone6 is 750x1334 and its px size is 375x667.
The real size is often > to the px size

On an iphone the device-width will be the same for landscape and portrait!

## What is viewport

The viewport is a virtual window where an app/website can be display. The viewport isn't equal by default to the real size or the px size but is bigger to be able to display all kind of website (zoom out). The viewport isn't define by the device but by the browser. You can calculate the zoom with device-width/viewport

To define the viewport the same size of the px size device (not the real size device):

<meta name="viewport" content="width=device-width">

Element bigger than the viewport extend the viewport.

Define the zoom:

<meta name="viewport" content="initial-scale=1.0">

The viewport as the same size as the device-width and the viewport doesn't change. If some elements are bigger they will not extend the viewport and won't display entirely.

## Font-size with viewport

font-size: 2 vh; is 2% of the viewport height

see: https://developer.mozilla.org/fr/docs/Mozilla/Mobile/Balise_meta_viewport

http://www.alsacreations.com/article/lire/1490-comprendre-le-viewport-dans-le-web-mobile.html

# Flexbox

define the container:

display: flex (or inline-flex); like block or inline
flex-flow: direction wrapping;
justify-content: options; how to display items
