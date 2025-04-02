---
title: ThemeColors class
linktitle: ThemeColors class
articleTitle: ThemeColors class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Themes.ThemeColors class. Represents the color scheme of the document theme which contains twelve colors."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Themes/themecolors/
---

## ThemeColors class

Represents the color scheme of the document theme which contains twelve colors.

[ThemeColors](./) object contains six accent colors, two dark colors, two light colors 
and a color for each of a hyperlink and followed hyperlink.




### Properties

| Name | Description |
| --- | --- |
| [accent1](./accent1/) | Specifies color Accent 1. |
| [accent2](./accent2/) | Specifies color Accent 2. |
| [accent3](./accent3/) | Specifies color Accent 3. |
| [accent4](./accent4/) | Specifies color Accent 4. |
| [accent5](./accent5/) | Specifies color Accent 5. |
| [accent6](./accent6/) | Specifies color Accent 6. |
| [dark1](./dark1/) | Specifies color Dark 1. |
| [dark2](./dark2/) | Specifies color Dark 2. |
| [followedHyperlink](./followedHyperlink/) | Specifies color for a clicked hyperlink. |
| [hyperlink](./hyperlink/) | Specifies color for a hyperlink. |
| [light1](./light1/) | Specifies color Light 1. |
| [light2](./light2/) | Specifies color Light 2. |

### Examples

Shows how to set custom colors and fonts for themes.

```js
let doc = new aw.Document(base.myDir + "Theme colors.docx");

// The "Theme" object gives us access to the document theme, a source of default fonts and colors.
let theme = doc.theme;

// Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
theme.majorFonts.latin = "Courier New";
theme.minorFonts.latin = "Agency FB";

// Other languages may also have their custom fonts in this theme.
expect(theme.majorFonts.complexScript).toEqual('');
expect(theme.majorFonts.eastAsian).toEqual('');
expect(theme.minorFonts.complexScript).toEqual('');
expect(theme.minorFonts.eastAsian).toEqual('');

// The "Colors" property contains the color palette from Microsoft Word,
// which appears when changing shading or font color.
// Apply custom colors to the color palette so we have easy access to them in Microsoft Word
// when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
// or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
let colors = theme.colors;
colors.dark1 = "#191970";
colors.light1 = "#98FB98";
colors.dark2 = "#4B0082";
colors.light2 = "#F0E68C";

colors.accent1 = "#FF4500";
colors.accent2 = "#FFA07A";
colors.accent3 = "#FFFF00";
colors.accent4 = "#FFD700";
colors.accent5 = "#8A2BE2";
colors.accent6 = "#9400D3";

// Apply custom colors to hyperlinks in their clicked and un-clicked states.
colors.hyperlink = "#000000";
colors.followedHyperlink = "#808080";

doc.save(base.artifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### See Also

* module [Aspose.Words.Themes](../)

