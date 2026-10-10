---
title: ThemeFonts class
linktitle: ThemeFonts class
articleTitle: ThemeFonts class
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeFonts class. Represents a collection of fonts in the font scheme, allowing to specify different fonts for different languages [ThemeFonts.latin](./latin/), [ThemeFonts.east_asian](./east_asian/) and [ThemeFonts.complex_script](./complex_script/)"
type: docs
weight: 50
url: /it/python-net/aspose.words.themes/themefonts/
---

## ThemeFonts class

Represents a collection of fonts in the font scheme, allowing to specify different fonts for different languages [ThemeFonts.latin](./latin/), [ThemeFonts.east_asian](./east_asian/) and [ThemeFonts.complex_script](./complex_script/).
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/python-net/working-with-styles-and-themes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [complex_script](./complex_script/) | Specifies font name for ComplexScript characters. |
| [east_asian](./east_asian/) | Specifies font name for EastAsian characters. |
| [latin](./latin/) | Specifies font name for Latin characters. |

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

