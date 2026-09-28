---
title: LoadOptions.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "LoadOptions.font_settings property. Allows to specify document font settings."
type: docs
weight: 60
url: /zh/python-net/aspose.words.loading/loadoptions/font_settings/
---

## LoadOptions.font_settings property

Allows to specify document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words
may resolve the fonts to perform font fallback.

If set to ``None``, default static font settings [FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how to designate font substitutes during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.font_settings = aw.fonts.FontSettings()
# 为 LoadOptions 对象设置字体替换规则。
# 如果我们正在加载的文档使用了我们没有的字体，
# 此规则将用已有的字体替代不可用的字体。
# 在这种情况下，所有对 "MissingFont" 的使用都将转换为 "Comic Sans MS"。
substitution_rule = load_options.font_settings.substitution_settings.table_substitution
substitution_rule.add_substitutes('MissingFont', ['Comic Sans MS'])
doc = aw.Document(file_name=MY_DIR + 'Missing font.html', load_options=load_options)
# 此时，此类文本仍将保持为 "MissingFont"。
# 字体替换将在我们渲染文档时进行。
self.assertEqual('MissingFont', doc.first_section.body.first_paragraph.runs[0].font.name)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.ResolveFontsBeforeLoadingDocument.pdf')
```

Shows how to apply font substitution settings while loading a document.

```python
# 创建一个 FontSettings 对象，用于替换 "Times New Roman" 字体
# 使用我们 "MyFonts" 文件夹中的 "Arvo" 字体。
font_settings = aw.fonts.FontSettings()
font_settings.set_fonts_folder(FONTS_DIR, False)
font_settings.substitution_settings.table_substitution.add_substitutes('Times New Roman', ['Arvo'])
# 将该 FontSettings 对象设置为新创建的 LoadOptions 对象的属性。
load_options = aw.loading.LoadOptions()
load_options.font_settings = font_settings
# 加载文档，然后使用字体替换将其渲染为 PDF。
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'LoadOptions.FontSettings.pdf')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

