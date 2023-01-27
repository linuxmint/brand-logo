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
<summary>3.1. Save as Plain SVG and use pixels as units</summary>

All these files are saved as plain SVG (Inkscape > File > Save As... Plain SVG). This makes the files smaller without loosing any important data. Except one information: all units are in pixels. And everything was made using round numbers here. Prior to doing any edit, please set your document and tool units to pixels and prefer round numbers.</details>

<details>
<summary>3.2. Be careful if you want to change the color</summary>

If you want to change the color for the "Lm" logo, open it in Inkscape and change it. There is nothing intricate there. But if you want to change the color on the name (i.e. "linuxmint"), you must change both the fill and the stroke color.

That stroke has some thickness and was added to increase the font weight. Thus, you need to change both the fill and the stroke color on the name or else you end up with a typography that gets "choked" by an outline overprint of a different color. This:  

![](90-preview/ring-name-BAD-EXAMPLE.png)

That's bad. To avoid this "choking" outline of a different color, set the stroke paint to the same color as the one used for the fill. You can change both of those fill and stroke colors in the same Fill and Stroke dialog (Shift+Ctrl+F), under 2 different tabs.

That was only for the "linuxmint" name. The "lm" logo itself has nothing special.</details>

<details>
<summary>3.3. Update those previews here on top of this README</summary>

The preview files are located in the `90-preview` sub-directory. The different logo versions that appear in `preview.svg` and `preview-names.svg` are placed there as a link. So, if you make changes to a logo that already exists, those changes are automatically applied in the SVG preview files. But you still have to update the PNG preview by an export. To get this, open Inkscape and do: File > Export page as PNG. Keep the same file name to replace the old PNG with your update.

GitHub now allows displaying of SVG files, but it doesn't work when there are linked images in it. That's why we need to export to PNG file format.

If you add or remove some logo version, you will have to edit the SVG preview file(s), or create new ones. And then you need to export to PNG, and make sure those PNGs appear correctly in this `README.md`.</details>