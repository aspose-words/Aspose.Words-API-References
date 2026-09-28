---
title: ThemeColors.light1 property
linktitle: light1 property
articleTitle: light1 property
second_title: Aspose.Words for Python
description: "ThemeColors.light1 property. Specifies color Light 1."
type: docs
weight: 110
url: /zh/python-net/aspose.words.themes/themecolors/light1/
---

## ThemeColors.light1 property

Specifies color Light 1.


```python
@property
def light1(self) -> aspose.pydrawing.Color:
    ...

@light1.setter
def light1(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# "Theme" 对象让我们访问文档主题，它是默认字体和颜色的来源。
theme = doc.theme
# 某些样式，例如 "Heading 1" 和 "Subtitle"，将继承这些字体。
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# 其他语言也可能在此主题中拥有自定义字体。
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# "Colors" 属性包含来自 Microsoft Word 的颜色调色板，
# 该调色板在更改底纹或字体颜色时出现。
# 将自定义颜色应用到颜色调色板，以便在 Microsoft Word 中轻松访问它们
# 例如，当我们通过 "Home" -> "Font" -> "Font Color" 更改字体颜色时，
# 或插入形状，然后通过 "Shape Format" -> "Shape Styles" 为其设置颜色。
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
# 为超链接的已点击和未点击状态应用自定义颜色。
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

