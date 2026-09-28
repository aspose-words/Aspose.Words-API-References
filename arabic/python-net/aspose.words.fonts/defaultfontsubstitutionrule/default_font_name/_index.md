---
title: DefaultFontSubstitutionRule.default_font_name property
linktitle: default_font_name property
articleTitle: default_font_name property
second_title: Aspose.Words for Python
description: "DefaultFontSubstitutionRule.default_font_name property. Gets or sets the default font name."
type: docs
weight: 10
url: /ar/python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
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
# مصادر الخطوط التي يستخدمها المستند تحتوي على الخط "Arial"، ولكن ليس "Arvo".
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# عيّن خاصية "DefaultFontName" إلى "Courier New" لت،
# أثناء عرض المستند، استخدم هذا الخط في جميع الحالات عندما لا يتوفر خط آخر.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# ستستخدم Aspose.Words الآن الخط الافتراضي بدلاً من أي خطوط مفقودة أثناء أي استدعاءات للعرض.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontName.pdf')
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# الحصول على قاعدة الاستبدال الافتراضية ضمن FontSettings.
# ستستبدل هذه القاعدة جميع الخطوط المفقودة بـ "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# تعيين بديل الخط الافتراضي إلى "Courier New".
default_font_substitution_rule.default_font_name = 'Courier New'
# باستخدام أداة بناء المستند، أضف بعض النص بخط لا نمتلكه لرؤية حدوث الاستبدال،
# ثم قم بتصيير النتيجة في ملف PDF.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

