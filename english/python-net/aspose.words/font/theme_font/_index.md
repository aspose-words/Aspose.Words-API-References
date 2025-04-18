﻿---
title: Font.theme_font property
linktitle: theme_font property
articleTitle: theme_font property
second_title: Aspose.Words for Python
description: "Font.theme_font property. Gets or sets the theme font in the applied font scheme that is associated with this [Font](../) object."
type: docs
weight: 480
url: /python-net/aspose.words/font/theme_font/
---

## Font.theme_font property

Gets or sets the theme font in the applied font scheme that is associated with this [Font](../) object.



```python
@property
def theme_font(self) -> aspose.words.themes.ThemeFont:
    ...

@theme_font.setter
def theme_font(self, value: aspose.words.themes.ThemeFont):
    ...

```

### Examples

Shows how to work with theme fonts and colors.

```python
doc = aw.Document()
# Define fonts for languages uses by default.
doc.theme.minor_fonts.latin = 'Algerian'
doc.theme.minor_fonts.east_asian = 'Aharoni'
doc.theme.minor_fonts.complex_script = 'Andalus'
font = doc.styles.get_by_name('Normal').font
print('Originally the Normal style theme color is: {0} and RGB color is: {1}\n'.format(font.theme_color, font.color))
# We can use theme font and color instead of default values.
font.theme_font = aw.themes.ThemeFont.MINOR
font.theme_color = aw.themes.ThemeColor.ACCENT2
self.assertEqual(aw.themes.ThemeFont.MINOR, font.theme_font)
self.assertEqual('Algerian', font.name)
self.assertEqual(aw.themes.ThemeFont.MINOR, font.theme_font_ascii)
self.assertEqual('Algerian', font.name_ascii)
self.assertEqual(aw.themes.ThemeFont.MINOR, font.theme_font_bi)
self.assertEqual('Andalus', font.name_bi)
self.assertEqual(aw.themes.ThemeFont.MINOR, font.theme_font_far_east)
self.assertEqual('Aharoni', font.name_far_east)
self.assertEqual(aw.themes.ThemeFont.MINOR, font.theme_font_other)
self.assertEqual('Algerian', font.name_other)
self.assertEqual(aw.themes.ThemeColor.ACCENT2, font.theme_color)
self.assertEqual(aspose.pydrawing.Color.empty(), font.color)
# There are several ways of reset them font and color.
# 1 -  By setting ThemeFont.None/ThemeColor.None:
font.theme_font = aw.themes.ThemeFont.NONE
font.theme_color = aw.themes.ThemeColor.NONE
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font)
self.assertEqual('Algerian', font.name)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_ascii)
self.assertEqual('Algerian', font.name_ascii)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_bi)
self.assertEqual('Andalus', font.name_bi)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_far_east)
self.assertEqual('Aharoni', font.name_far_east)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_other)
self.assertEqual('Algerian', font.name_other)
self.assertEqual(aw.themes.ThemeColor.NONE, font.theme_color)
self.assertEqual(aspose.pydrawing.Color.empty(), font.color)
# 2 -  By setting non-theme font/color names:
font.name = 'Arial'
font.color = aspose.pydrawing.Color.blue
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font)
self.assertEqual('Arial', font.name)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_ascii)
self.assertEqual('Arial', font.name_ascii)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_bi)
self.assertEqual('Arial', font.name_bi)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_far_east)
self.assertEqual('Arial', font.name_far_east)
self.assertEqual(aw.themes.ThemeFont.NONE, font.theme_font_other)
self.assertEqual('Arial', font.name_other)
self.assertEqual(aw.themes.ThemeColor.NONE, font.theme_color)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), font.color.to_argb())
```

Shows how to create and use themed style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln()
# Create some style with theme font properties.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'ThemedStyle')
style.font.theme_font = aw.themes.ThemeFont.MAJOR
style.font.theme_color = aw.themes.ThemeColor.ACCENT5
style.font.tint_and_shade = 0.3
builder.paragraph_format.style_name = 'ThemedStyle'
builder.writeln('Text with themed style')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

