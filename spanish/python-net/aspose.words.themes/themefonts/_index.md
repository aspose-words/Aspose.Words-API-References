---
title: ThemeFonts class
linktitle: ThemeFonts class
articleTitle: ThemeFonts class
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeFonts class. Represents a collection of fonts in the font scheme, allowing to specify different fonts for different languages [ThemeFonts.latin](./latin/), [ThemeFonts.east_asian](./east_asian/) and [ThemeFonts.complex_script](./complex_script/)"
type: docs
weight: 50
url: /es/python-net/aspose.words.themes/themefonts/
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
# El objeto "Theme" nos brinda acceso al tema del documento, una fuente de fuentes y colores predeterminados.
theme = doc.theme
# Algunos estilos, como "Heading 1" y "Subtitle", heredarán estas fuentes.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Otros idiomas también pueden tener sus fuentes personalizadas en este tema.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# La propiedad "Colors" contiene la paleta de colores de Microsoft Word,
# que aparece al cambiar el sombreado o el color de fuente.
# Aplica colores personalizados a la paleta de colores para que tengamos fácil acceso a ellos en Microsoft Word
# cuando, por ejemplo, cambiamos el color de fuente a través de "Home" -> "Font" -> "Font Color",
# o insertamos una forma, y luego establecemos un color para ella a través de "Shape Format" -> "Shape Styles".
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
# Aplica colores personalizados a los hipervínculos en sus estados pulsado y sin pulsar.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../)

