---
title: ThemeFonts.east_asian property
linktitle: east_asian property
articleTitle: east_asian property
second_title: Aspose.Words for Python
description: "ThemeFonts.east_asian property. Specifies font name for EastAsian characters."
type: docs
weight: 20
url: /fr/python-net/aspose.words.themes/themefonts/east_asian/
---

## ThemeFonts.east_asian property

Specifies font name for EastAsian characters.


```python
@property
def east_asian(self) -> str:
    ...

@east_asian.setter
def east_asian(self, value: str):
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# L'objet "Theme" nous donne accès au thème du document, une source de polices et de couleurs par défaut.
theme = doc.theme
# Certaines styles, comme "Heading 1" et "Subtitle", hériteront de ces polices.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# D'autres langues peuvent également avoir leurs polices personnalisées dans ce thème.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# La propriété "Colors" contient la palette de couleurs de Microsoft Word,
# qui apparaît lors du changement d’ombrage ou de couleur de police.
# Appliquez des couleurs personnalisées à la palette de couleurs afin d’y accéder facilement dans Microsoft Word
# lorsque nous, par exemple, changeons la couleur de police via "Home" -> "Font" -> "Font Color",
# ou insérons une forme, puis définissons une couleur pour celle-ci via "Shape Format" -> "Shape Styles".
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
# Appliquez des couleurs personnalisées aux hyperliens dans leurs états cliqué et non cliqué.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeFonts](../)

