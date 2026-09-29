---
title: ThemeColors class
linktitle: ThemeColors class
articleTitle: ThemeColors class
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeColors class. Represents the color scheme of the document theme which contains twelve colors."
type: docs
weight: 30
url: /sv/python-net/aspose.words.themes/themecolors/
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

* module [aspose.words.themes](../)

