---
title: Font.theme_color property
linktitle: theme_color property
articleTitle: theme_color property
second_title: Aspose.Words for Python
description: "Font.theme_color property. Gets or sets the theme color in the applied color scheme that is associated with this [Font](../) object."
type: docs
weight: 470
url: /zh/python-net/aspose.words/font/theme_color/
---

## Font.theme_color property

Gets or sets the theme color in the applied color scheme that is associated with this [Font](../) object.



```python
@property
def theme_color(self) -> aspose.words.themes.ThemeColor:
    ...

@theme_color.setter
def theme_color(self, value: aspose.words.themes.ThemeColor):
    ...

```

### Examples

Shows how to work with theme fonts and colors.

```python
doc = aw.Document()
# 为默认使用的语言定义字体。
doc.theme.minor_fonts.latin = 'Algerian'
doc.theme.minor_fonts.east_asian = 'Aharoni'
doc.theme.minor_fonts.complex_script = 'Andalus'
font = doc.styles.get_by_name('Normal').font
print('Originally the Normal style theme color is: {0} and RGB color is: {1}\n'.format(font.theme_color, font.color))
# 我们可以使用主题字体和颜色来替代默认值。
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
# 有多种方法可以重置它们的字体和颜色。
# 1 - 通过设置 ThemeFont.None/ThemeColor.None：
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
# 2 - 通过设置非主题的字体/颜色名称：
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
# 使用主题字体属性创建一些样式。
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

