---
title: ThemeColors.dark2 property
linktitle: dark2 property
articleTitle: dark2 property
second_title: Aspose.Words for Python
description: "ThemeColors.dark2 property. Specifies color Dark 2."
type: docs
weight: 80
url: /de/python-net/aspose.words.themes/themecolors/dark2/
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
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# Das "Theme"-Objekt gibt uns Zugriff auf das Dokumententhema, eine Quelle für Standardschriften und -farben.
theme = doc.theme
# Einige Stile, wie "Heading 1" und "Subtitle", erben diese Schriften.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Andere Sprachen können ebenfalls ihre eigenen Schriften in diesem Thema haben.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# Die "Colors"-Eigenschaft enthält die Farbpalette von Microsoft Word,
# die erscheint, wenn Sie Schattierung oder Schriftfarbe ändern.
# Wenden Sie benutzerdefinierte Farben auf die Farbpalette an, damit wir in Microsoft Word einfachen Zugriff darauf haben
# wenn wir zum Beispiel die Schriftfarbe über "Home" -> "Font" -> "Font Color" ändern,
# oder eine Form einfügen und dann über "Shape Format" -> "Shape Styles" eine Farbe dafür festlegen.
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
# Wenden Sie benutzerdefinierte Farben auf Hyperlinks in ihren angeklickten und nicht angeklickten Zuständen an.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

