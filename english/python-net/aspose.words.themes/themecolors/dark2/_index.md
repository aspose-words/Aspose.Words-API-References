---
title: ThemeColors.dark2 property
linktitle: dark2 property
articleTitle: dark2 property
second_title: Aspose.Words for Python
description: "ThemeColors.dark2 property. Specifies color Dark 2."
type: docs
weight: 80
url: /python-net/aspose.words.themes/themecolors/dark2/
---

## ThemeColors.dark2 property

Specifies color Dark 2.


```python
@property
def dark2(self) -> aspose.pydrawing.Color:
    ...

@dark2.setter
def dark2(self, value: aspose.pydrawing.Color):
    ...

```

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

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

