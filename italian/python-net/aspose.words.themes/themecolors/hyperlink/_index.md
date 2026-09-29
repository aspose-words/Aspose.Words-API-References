---
title: ThemeColors.hyperlink property
linktitle: hyperlink property
articleTitle: hyperlink property
second_title: Aspose.Words for Python
description: "ThemeColors.hyperlink property. Specifies color for a hyperlink."
type: docs
weight: 100
url: /it/python-net/aspose.words.themes/themecolors/hyperlink/
---

## ThemeColors.hyperlink property

Specifies color for a hyperlink.


```python
@property
def hyperlink(self) -> aspose.pydrawing.Color:
    ...

@hyperlink.setter
def hyperlink(self, value: aspose.pydrawing.Color):
    ...

```

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

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

