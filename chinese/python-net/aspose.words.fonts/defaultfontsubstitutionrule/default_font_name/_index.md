---
title: DefaultFontSubstitutionRule.default_font_name property
linktitle: default_font_name property
articleTitle: default_font_name property
second_title: Aspose.Words for Python
description: "DefaultFontSubstitutionRule.default_font_name property. Gets or sets the default font name."
type: docs
weight: 10
url: /zh/python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
---

## DefaultFontSubstitutionRule.default_font_name property

Gets or sets the default font name.


```python
@property
def default_font_name(self) -> str:
    ...

@default_font_name.setter
def default_font_name(self, value: str):
    ...

```

### Remarks

The default value is 'Times New Roman'.




### Examples

Shows how to specify a default font.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Arvo'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# 文档使用的字体源包含字体 "Arial"，但不包含 "Arvo"。
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# 将 "DefaultFontName" 属性设置为 "Courier New"，以
# 在渲染文档时，当其他字体不可用时，在所有情况下使用该字体。
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Aspose.Words 现在将在任何渲染调用中使用默认字体来替代缺失的字体。
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontName.pdf')
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# 获取 FontSettings 中的默认替换规则。
# 此规则会将所有缺失的字体替换为 "Times New Roman"。
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# 将默认字体替代设置为 "Courier New"。
default_font_substitution_rule.default_font_name = 'Courier New'
# 使用文档生成器，添加一些我们没有的字体的文本，以观察替换的发生，
# 然后将结果渲染为 PDF。
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

