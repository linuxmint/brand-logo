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
<summary>3.1. How to change the color (click to expand)</summary>

If you want to change the color, you can do this in Inkscape, using the Fill and Stroke dialog (Shift+Ctrl+F).

Alternately, you could just use any simple text editor to search and replace the current official color all across the SVG file. In the SVG files, the colors are written in hex format (hex = short for hexadecimal). For example, the current official color, at the time of this writing, is set as `#86be43`. (Prefer using lower case letters.) 

So, you could just open some logo such as "ring-name.svg" in some simple text editor, such as Xed or Gedit. And then do a search and replace from `#86be43` to... say `#123abc` for example. It doesn't work? It is quite possible we moved to some other color. You can use any color picker to find which color we are currently using. Just make sure you set your color picker to express colors in hex values, and with lower case letters: `#123abc`, for example.

Now, if you want to change the color on all logo versions, all at once and avoiding any mistake, use those simple CLI:

```
cd $HOME/brand-logo # Go where you downloaded or cloned
sed -i 's/\#86be43/\#123abc/g' *.svg # replace 86be43 and 123abc as needed
```
</details>

<details>
<summary>3.2. Update those previews here on top of this README (click to expand)</summary>

The preview files are located in the `90-preview` sub-directory. The different logo versions that appear in `preview.svg` and `preview-names.svg` are placed there as a link. So, if you make changes to a logo that already exists, those changes are automatically applied in the SVG preview files. But you still have to update the PNG preview by doing an export. To get this, open Inkscape and do: File > Export page as PNG. Keep the same file name to replace the old PNG with your update.

Alternately, you can update the various `preview*.png` all at once. Using those simple CLI:

```
cd 90-preview # Go to $HOME/brand-logo/90-preview
rm preview*.png; inkscape --export-type=png preview*.svg
```

NOTE: GitHub now allows displaying of SVG files, but it doesn't work when there are linked images in it. That's why we need to export to PNG file format.
</details>