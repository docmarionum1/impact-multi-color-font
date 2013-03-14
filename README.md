impact-multi-color-font
=======================

A plugin for the [ImpactJS Game Engine](http://impactjs.com) to allow for arbitrary font colors at runtime, rather than the current system which requires a different font imagemap for each color.

## Usage

Download `multi-color-font.js` into your project's plugin directory and then include `plugins.multi-color-font` in your `main.js` require section.

When you instantiate a font, you can optionally include a list of colors that you want to use:

```
new ig.Font( 'media/fonts/04b03.font_big.png', ["FFFFFF", "000000", "FF0000"] )
```

The colors must be in hexadecimal format and have no leading '#' (hash).  Any colors that you want to use with the font must be listed during instatiation.  The first color listed will be the "default" color.  If no list of colors is passed to the Font, then it will default to having only white.

Then, when drawing text with the font, a color can be passed to the draw function:

```
font.draw("Hello World", 0, 0, ig.Font.ALIGN.CENTER, "FF0000")
```

If no color is specified, the default color will be used.  That is either the first color in the list you specified or white if no color list was given. 
