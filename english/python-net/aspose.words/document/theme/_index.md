---
title: Document.theme property
linktitle: theme property
articleTitle: theme property
second_title: Aspose.Words for Python
description: "Document.theme property. Gets the [Document.theme](./) object for this document."
type: docs
weight: 430
url: /python-net/aspose.words/document/theme/
---

## Document.theme property

Gets the [Document.theme](./) object for this document.



```python
@property
def theme(self) -> aspose.words.themes.Theme:
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

* module [aspose.words](../../)
* class [Document](../)

