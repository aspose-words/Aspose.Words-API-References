---
title: ThemeColors.accent5 property
linktitle: accent5 property
articleTitle: accent5 property
second_title: Aspose.Words for Python
description: "ThemeColors.accent5 property. Specifies color Accent 5."
type: docs
weight: 50
url: /python-net/aspose.words.themes/themecolors/accent5/
---

## ThemeColors.accent5 property

Specifies color Accent 5.


```python
@property
def accent5(self) -> aspose.pydrawing.Color:
    ...

@accent5.setter
def accent5(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# The "Theme" object gives us access to the document theme, a source of default fonts and colors.
theme = doc.theme
# Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Other languages may also have their custom fonts in this theme.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# The "Colors" property contains the color palette from Microsoft Word,
# which appears when changing shading or font color.
# Apply custom colors to the color palette so we have easy access to them in Microsoft Word
# when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
# or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
colors = theme.colors
colors.dark1 = aspose.pydrawing.Color.midnight_blue
colors.light1 = aspose.pydrawing.Color.pale_green
colors.dark2 = aspose.pydrawing.Color.indigo
colors.light2 = aspose.pydrawing.Color.khaki
colors.accent1 = aspose.pydrawing.Color.orange_red
colors.accent2 = aspose.pydrawing.Color.light_salmon
colors.accent3 = aspose.pydrawing.Color.yellow
colors.accent4 = aspose.pydrawing.Color.gold
colors.accent5 = aspose.pydrawing.Color.blue_violet
colors.accent6 = aspose.pydrawing.Color.dark_violet
# Apply custom colors to hyperlinks in their clicked and un-clicked states.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

