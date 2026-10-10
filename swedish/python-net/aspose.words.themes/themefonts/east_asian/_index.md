---
title: ThemeFonts.east_asian property
linktitle: east_asian property
articleTitle: east_asian property
second_title: Aspose.Words for Python
description: "ThemeFonts.east_asian property. Specifies font name for EastAsian characters."
type: docs
weight: 20
url: /sv/python-net/aspose.words.themes/themefonts/east_asian/
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
* class [ThemeFonts](../)

