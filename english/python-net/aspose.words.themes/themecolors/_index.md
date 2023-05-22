---
title: ThemeColors class
linktitle: ThemeColors class
articleTitle: ThemeColors class
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeColors class. Represents the color scheme of the document theme which contains twelve colors."
type: docs
weight: 30
url: /python-net/aspose.words.themes/themecolors/
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
| [followed_hyperlink](./followed_hyperlink/) | Specifies color for a clicked hyperlink. |
| [hyperlink](./hyperlink/) | Specifies color for a hyperlink. |
| [light1](./light1/) | Specifies color Light 1. |
| [light2](./light2/) | Specifies color Light 2. |

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(MY_DIR + "Theme colors.docx")

# The "theme" object gives us access to the document theme, a source of default fonts and colors.
theme = doc.theme

# Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
theme.major_fonts.latin = "Courier New"
theme.minor_fonts.latin = "Agency FB"

# Other languages may also have their custom fonts in this theme.
self.assertEqual("", theme.major_fonts.complex_script)
self.assertEqual("", theme.major_fonts.east_asian)
self.assertEqual("", theme.minor_fonts.complex_script)
self.assertEqual("", theme.minor_fonts.east_asian)

# The "colors" property contains the color palette from Microsoft Word,
# which appears when changing shading or font color.
# Apply custom colors to the color palette so we have easy access to them in Microsoft Word
# when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
# or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
colors = theme.colors
colors.dark1 = drawing.Color.midnight_blue
colors.light1 = drawing.Color.pale_green
colors.dark2 = drawing.Color.indigo
colors.light2 = drawing.Color.khaki

colors.accent1 = drawing.Color.orange_red
colors.accent2 = drawing.Color.light_salmon
colors.accent3 = drawing.Color.yellow
colors.accent4 = drawing.Color.gold
colors.accent5 = drawing.Color.blue_violet
colors.accent6 = drawing.Color.dark_violet

# Apply custom colors to hyperlinks in their clicked and un-clicked states.
colors.hyperlink = drawing.Color.black
colors.followed_hyperlink = drawing.Color.gray

doc.save(ARTIFACTS_DIR + "Themes.custom_colors_and_fonts.docx")
```

### See Also

* module [aspose.words.themes](../)

