---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /ar/python-net/aspose.words/document/font_settings/
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
# مصادر الخط الافتراضية تحتوي على الخط الأول الذي يستخدمه المستند.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# الخط الثاني، "Amethysta"، غير متوفر.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# يمكننا تكوين جدول استبدال الخطوط الذي يحدد
# أي الخطوط سيستخدمها Aspose.Words كبدائل للخطوط غير المتوفرة.
# حدد خطين بديلين لـ "Amethysta": "Arvo" و "Courier New".
# إذا كان البديل الأول غير متوفر، يحاول Aspose.Words استخدام البديل الثاني، وهكذا.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" غير متوفر، وقاعدة الاستبدال تنص على أن الخط الأول لاستخدامه كبديل هو "Arvo".
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" غير متوفر أيضًا، لكن "Courier New" متوفر.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# سوف يعرض المستند الناتج النص الذي يستخدم خط "Amethysta" مُنسقًا بخط "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

