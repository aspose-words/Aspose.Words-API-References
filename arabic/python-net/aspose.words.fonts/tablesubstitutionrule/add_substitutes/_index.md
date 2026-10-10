---
title: TableSubstitutionRule.add_substitutes method
linktitle: add_substitutes method
articleTitle: add_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.add_substitutes method. Adds substitute font names for given original font name."
type: docs
weight: 10
url: /ar/python-net/aspose.words.fonts/tablesubstitutionrule/add_substitutes/
---

## add_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Adds substitute font names for given original font name.


```python
def add_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

Shows how to access a document's system font source and set font substitutes.

```python
import platform
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR

class TestFontSubstitution(ApiExampleBase):

    def test_font_substitution(self):
        doc = aw.Document()
        doc.font_settings = aw.fonts.FontSettings()
        # بشكل افتراضي، يحتوي المستند الفارغ دائمًا على مصدر خط نظام.
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        system_font_source = doc.font_settings.get_fonts_sources()[0].as_system_font_source()
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
        self.assertEqual(0, system_font_source.priority)
        is_windows = platform.system() == 'Windows'
        if is_windows:
            fonts_path = 'C:\\WINDOWS\\Fonts'
            actual = None
            cond_expression = next(iter(aw.fonts.SystemFontSource.get_system_font_folders()), None)
            if cond_expression is not None:
                actual = cond_expression.lower()
            self.assertEqual(fonts_path.lower(), actual)
        for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():
            print(system_font_folder)
        # حدد خطًا موجودًا في دليل خطوط Windows كبديل لخط غير موجود.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # بدلاً من ذلك، يمكننا إضافة مصدر خط من مجلد يحتوي على الخط المقابل.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # إعادة ضبط مصادر الخط لا يزال يتركنا مع مصدر خط النظام بالإضافة إلى بدائلنا.
        doc.font_settings.reset_font_sources()
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertTrue(doc.font_settings.substitution_settings.font_name_substitution.enabled)
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

