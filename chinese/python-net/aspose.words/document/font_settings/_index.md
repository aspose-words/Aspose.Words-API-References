---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /zh/python-net/aspose.words/document/font_settings/
---

## Document.font_settings property

Gets or sets document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

This property allows to specify font settings per document. If set to ``None``, default static font settings
[FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# 默认字体来源包含文档使用的第一种字体。
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# 第二种字体 "Amethysta" 不可用。
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# 我们可以配置一个字体替代表，用于确定
# Aspose.Words 将使用哪些字体作为不可用字体的替代。
# 为 "Amethysta" 设置两个替代字体："Arvo" 和 "Courier New"。
# 如果第一个替代不可用，Aspose.Words 将尝试使用第二个替代，依此类推。
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" 不可用，替代规则规定第一个使用的替代字体是 "Arvo"。
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" 也不可用，但 "Courier New" 可用。
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# 输出文档将显示使用 "Amethysta" 字体但以 "Courier New" 格式化的文本。
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

