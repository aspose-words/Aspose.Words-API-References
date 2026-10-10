---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /ar/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
---

## set_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Override substitute font names for given original font name.


```python
def set_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

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

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# أنشئ قاعدة استبدال جدول جديدة وحمّل جدول استبدال خطوط Windows الافتراضي.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# إذا اخترنا الخطوط حصريًا من مجلدنا، سنحتاج إلى جدول استبدال مخصص.
# لن نتمكن بعد الآن من الوصول إلى خطوط Microsoft Windows،
# مثل "Arial" أو "Times New Roman" لأنها غير موجودة في مجلد الخطوط الجديد لدينا.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# فيما يلي طريقتان لتحميل جدول استبدال من ملف في نظام الملفات المحلي.
# 1 -  من تدفق:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  مباشرةً من ملف:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# نظرًا لأننا لم نعد نملك الوصول إلى "Arial"، سيحاول جدول الخطوط أولاً استبداله بـ "Nonexistent Font".
# ليس لدينا هذا الخط لذا سيتحول إلى البديل التالي، "Kreon"، الموجود في مجلد "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# يمكننا توسيع هذا الجدول برمجيًا. سنضيف إدخالًا يستبدل "Times New Roman" بـ "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# يمكننا إضافة بديل احتياطي ثانوي لإدخال خط موجود باستخدام AddSubstitutes().
# في حال عدم توفر "Arvo"، سيبحث جدولنا عن "M+ 2m" كخيار بديل ثانٍ.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# يمكن لـ SetSubstitutes() تعيين قائمة جديدة من الخطوط البديلة لخط معين.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# كتابة النص بخطوط لا نمتلك إمكانية الوصول إليها ستستدعي قواعد الاستبدال لدينا.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Text written in Arial, to be substituted by Kreon.')
builder.font.name = 'Times New Roman'
builder.writeln('Text written in Times New Roman, to be substituted by Squarish Sans CT.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Custom.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

