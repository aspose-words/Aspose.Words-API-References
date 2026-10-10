---
title: ThemeColors class
linktitle: ThemeColors class
articleTitle: ThemeColors class
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeColors class. Represents the color scheme of the document theme which contains twelve colors."
type: docs
weight: 30
url: /it/python-net/aspose.words.themes/themecolors/
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
# L'oggetto "Theme" ci dà accesso al tema del documento, una fonte di caratteri e colori predefiniti.
theme = doc.theme
# Alcuni stili, come "Heading 1" e "Subtitle", erediteranno questi caratteri.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Altre lingue possono anche avere i loro caratteri personalizzati in questo tema.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# La proprietà "Colors" contiene la tavolozza dei colori di Microsoft Word,
# che appare quando si modifica l'ombreggiatura o il colore del carattere.
# Applica colori personalizzati alla tavolozza dei colori così da averne un facile accesso in Microsoft Word
# quando, ad esempio, cambiamo il colore del carattere tramite "Home" -> "Font" -> "Font Color",
# o inseriamo una forma, e poi impostiamo un colore per essa tramite "Shape Format" -> "Shape Styles".
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
# Applica colori personalizzati ai collegamenti ipertestuali nei loro stati cliccato e non cliccato.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../)

