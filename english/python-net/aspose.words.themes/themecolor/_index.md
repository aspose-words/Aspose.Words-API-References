---
title: ThemeColor enumeration
linktitle: ThemeColor enumeration
articleTitle: ThemeColor enumeration
second_title: Aspose.Words for Python
description: "aspose.words.themes.ThemeColor enumeration. Specifies the theme colors for document themes"
type: docs
weight: 20
url: /python-net/aspose.words.themes/themecolor/
---

## ThemeColor enumeration

Specifies the theme colors for document themes.
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/python-net/working-with-styles-and-themes/) documentation article.



The specified theme color is a reference to one of the predefined theme colors, located in the
document's Theme part, which allows color information to be set centrally in the document.


### Members

| Name | Description |
| --- | --- |
| NONE | No color. |
| DARK1 | Dark main color 1. |
| LIGHT1 | Light main color 1. |
| DARK2 | Dark main color 2. |
| LIGHT2 | Light main color 2. |
| ACCENT1 | Accent color 1. |
| ACCENT2 | Accent color 2. |
| ACCENT3 | Accent color 3. |
| ACCENT4 | Accent color 4. |
| ACCENT5 | Accent color 5. |
| ACCENT6 | Accent color 6. |
| HYPERLINK | Hyperlink color. |
| FOLLOWED_HYPERLINK | Followed hyperlink color. |
| TEXT1 | Text color 1. |
| TEXT2 | Text color 2. |
| BACKGROUND1 | Background color 1. |
| BACKGROUND2 | Background color 2. |

### Examples

Shows how to create and use themed style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln()
# Create some style with theme font properties.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'ThemedStyle')
style.font.theme_font = aw.themes.ThemeFont.MAJOR
style.font.theme_color = aw.themes.ThemeColor.ACCENT5
style.font.tint_and_shade = 0.3
builder.paragraph_format.style_name = 'ThemedStyle'
builder.writeln('Text with themed style')
```

Shows how to work with theme fonts and colors.

```python
doc = aw.Document()
# Define fonts for languages uses by default.
doc.theme.minor_fonts.latin = 'Algerian'
doc.theme.minor_fonts.east_asian = 'Aharoni'
doc.theme.minor_fonts.complex_script = 'Andalus'
font = doc.styles.get_by_name('Normal').font
print(f'Originally the Normal style theme color is: {font.theme_color} and RGB color is: {font.color}\n')
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
# 1 -  By setting ThemeFont.NONE/ThemeColor.NONE:
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

### See Also

* module [aspose.words.themes](../)

