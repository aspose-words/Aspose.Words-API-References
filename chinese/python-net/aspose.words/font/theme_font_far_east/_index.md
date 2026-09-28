---
title: Font.theme_font_far_east property
linktitle: theme_font_far_east property
articleTitle: theme_font_far_east property
second_title: Aspose.Words for Python
description: "Font.theme_font_far_east property. Gets or sets the East Asian theme font in the applied font scheme that is associated with this [Font](../) object."
type: docs
weight: 510
url: /zh/python-net/aspose.words/font/theme_font_far_east/
---

## Font.theme_font_far_east property

Gets or sets the East Asian theme font in the applied font scheme that is associated with this [Font](../) object.



```python
@property
def theme_font_far_east(self) -> aspose.words.themes.ThemeFont:
    ...

@theme_font_far_east.setter
def theme_font_far_east(self, value: aspose.words.themes.ThemeFont):
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

### See Also

* module [aspose.words](../../)
* class [Font](../)

