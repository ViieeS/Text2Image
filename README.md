**Text2Image** — component for convert text to image using ttf fonts. Might be helpful for security purpose against spam-bots personal data scanners (e.g. email and phone numbers).
Also you can make image placeholder, like placehold.it service.

##Examples

Call snippet:
```
[[!Text2Image?text=`Hello World!`]]
```
By default generates a simple PNG image with transparent background in base64 encoding.

![Text2Image Example: Hello World!](https://file.modx.pro/files/0/5/d/05dcbf23b7b635485cc035883c9c2d5c.png)

Generates a placeholder image 100x100 pixels:

```
<img src="[[!DummyImage?size=`100x100`]]" alt="100x100" />
```
![Text2Image Example: Placeholder 100x100](https://file.modx.pro/files/9/3/1/9310fc072b7af00b019452d8a8ad3128.png)

You can specify the text color, font, size, angle, space, background color and image size in snippet parameters.
Snippet call with different parameters:
```
[[!Text2Image?
    &text=`Text2Image`
    &color=`#FFD700`
    &bg=`#000`
    &angle=`-45`
    &format=`jpeg`
    &fontFile=`[[+assetsPath]]fonts/myFavouriteFont.ttf`
]]
```

![Text2Image Example with different parameters](https://file.modx.pro/files/b/e/e/beedc32578b5e64b1e1582283a348a07.png)

You can upload your own fonts, for this purpose you need to specify the path to the font, using `[[++assets_path]]` placeholder . Or put your font to the component fonts directory: /assets/components/text2image/fonts, then the path should be, as in the example above using the placeholder `[[+assetsPath]]`.

##Parameters list

* **angle** — The angle in degrees, with 0 degrees being left-to-right reading text. Higher values represent a counter-clockwise rotation. For example, a value of 90 would result in bottom-to-top reading text.
* **bg** — The background color in HEX (#fff).
* **break** — Wraps a string to a given number of characters.
* **color** — The font color in HEX (#000).
* **fontFile** — The path to the TrueType font you wish to use (.ttf).
* **fontSize** — The font size in points (pt).
* **format** — The image format (png,gif,jpeg).
* **h** — The image height.
* **padding** — The Padding for text on image.
* **toPlaceholder** — If set, will output the content to the placeholder specified in this property, rather than outputting the content directly.
* **tpl** — The chunk to use for each row of image..
* **trp** — The background transparent.
* **w** — The image width