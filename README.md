# Linux Mint logo and brand resources

![90-preview/preview.png](90-preview/preview.png)

![90-preview/preview-names.png](90-preview/preview-names.png)

▲ *Different logo variants pictured with different backgrounds.*

---

### 1. Download them all into a small ZIP

![](90-preview/GitHub-code-button.png)

* Click on the green **Code** button on the top-right ↗ of the [main page](https://github.com/linuxmint/brand-logo) and then **Download ZIP.**
* Or clone it: `git clone https://github.com/linuxmint/brand-logo.git`.

### 2. Prefer SVG format whenever possible

SVG stands for Scalable Vector Graphics. They will always be displayed perfectly at any size, large or small. And these are the source files. They can be changed. You can easily change shapes or colors. And they are very lightweight, thus very fast on the internet.

### 3. How to modify or add new logo versions

<details>
<summary>3.1. Be careful if you want to change the color (click to expand)</summary>

If you want to change the color on the "Lm" logo, open it in Inkscape and change it. There is nothing intricate there. But if you want to change the color on the name (i.e. "linuxmint"), you must change both the fill and the stroke color.

That stroke has some thickness and was added to increase the font weight. Thus, you need to change both the fill and the stroke color on the name or else you end up with a typography that gets "choked" by an outline overprint of a different color. This:  

![](90-preview/ring-name-BAD-EXAMPLE.png)

That's bad. To avoid this "choking" outline of a different color, set the stroke paint to the same color as the one used for the fill. You can change both of those fill and stroke colors in the same Fill and Stroke dialog (Shift+Ctrl+F), under 2 different tabs, in Inkscape.

Alternately, you could just use any simple text editor to search and replace the current official color all across the SVG file. This works for the name and for the logo. In the SVG files, the colors are written in hex format (hex = short for hexadecimal). For example, the current official color, at the time of this writing, is set as `#86be43`. (Prefer using lower case letters.) 

So, you could just open some logo such as "ring-name.svg" in some simple text editor, such as Xed or Gedit. And then do a search and replace from `#86be43` to... say `#123abc` for example. It doesn't work? It is quite possible we moved to some other color. You can use any color picker to find which color we are currently using. Just make sure you set your color picker to express colors in hex values, and with lower case letters: `#123abc`, for example.

And, if you want to change the color on many logo versions, and you hate doing repetitive work, then you could just use some simple terminal command to do so. Example:  

```
cd ~/Downloads/brand-logo-master # go where you downloaded and extracted
sed -i 's/\#86be43/\#123abc/g' *.svg # replace 86be43 and 123abc as needed
```

You've just changed all logo files in a split second !
</details>

<details>
<summary>3.2. Update those previews here on top of this README (click to expand)</summary>

The preview files are located in the `90-preview` sub-directory. The different logo versions that appear in `preview.svg` and `preview-names.svg` are placed there as a link. So, if you make changes to a logo that already exists, those changes are automatically applied in the SVG preview files. But you still have to update the PNG preview by an export. To get this, open Inkscape and do: File > Export page as PNG. Keep the same file name to replace the old PNG with your update.

GitHub now allows displaying of SVG files, but it doesn't work when there are linked images in it. That's why we need to export to PNG file format.

If you add or remove some logo version, you will have to edit the SVG preview file(s), or create new ones. And then you need to export to PNG, and make sure those PNGs appear correctly in this `README.md`.
</details>