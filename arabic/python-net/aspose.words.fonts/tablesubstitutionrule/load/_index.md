---
title: TableSubstitutionRule.load method
linktitle: load method
articleTitle: load method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.TableSubstitutionRule.load method"
type: docs
weight: 30
url: /ar/python-net/aspose.words.fonts/tablesubstitutionrule/load/
---

## load(file_name) {#str}

Loads table substitution settings from XML file.


```python
def load(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Input file name. |

## load(stream) {#bytesio}

Loads table substitution settings from XML stream.


```python
def load(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Input stream. |

## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

