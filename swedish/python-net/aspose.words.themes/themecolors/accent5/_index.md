---
title: ThemeColors.accent5 property
linktitle: accent5 property
articleTitle: accent5 property
second_title: Aspose.Words for Python
description: "ThemeColors.accent5 property. Specifies color Accent 5."
type: docs
weight: 50
url: /sv/python-net/aspose.words.themes/themecolors/accent5/
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
# Objektet "Theme" ger oss åtkomst till dokumenttemat, en källa till standardteckensnitt och färger.
theme = doc.theme
# Vissa stilar, såsom "Heading 1" och "Subtitle", kommer att ärva dessa teckensnitt.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Andra språk kan också ha sina egna teckensnitt i detta tema.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# Egenskapen "Colors" innehåller färgpaletten från Microsoft Word,
# som visas när du ändrar skuggning eller teckensnittsfärg.
# Applicera anpassade färger på färgpaletten så att vi har enkel åtkomst till dem i Microsoft Word
# när vi till exempel ändrar teckensnittsfärgen via "Home" -> "Font" -> "Font Color",
# eller infogar en form och sedan ställer in en färg för den via "Shape Format" -> "Shape Styles".
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
# Applicera anpassade färger på hyperlänkar i deras klickade och oklickade tillstånd.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

