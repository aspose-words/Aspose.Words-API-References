---
title: FontSettings.set_fonts_folder method
linktitle: set_fonts_folder method
articleTitle: set_fonts_folder method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folder method. Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts"
type: docs
weight: 80
url: /ar/python-net/aspose.words.fonts/fontsettings/set_fonts_folder/
---

## set_fonts_folder(font_folder, recursive) {#str_bool}

Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.
This is a shortcut to [FontSettings.set_fonts_folders()](../set_fonts_folders/#strlist_bool) for setting only one font directory.



```python
def set_fonts_folder(self, font_folder: str, recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_folder | str | The folder that contains TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Examples

Shows how to set a font source directory.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arvo'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# مصادر الخطوط لدينا لا تحتوي على الخط الذي استخدمناه للنص في هذا المستند.
# إذا استخدمنا إعدادات الخط هذه أثناء تصيير هذا المستند،
# ستطبق Aspose.Words خطًا احتياطيًا على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد موقعه.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# مصادر الخطوط الافتراضية تفتقد الخطين الذين نستخدمهما في هذا المستند.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# استخدم طريقة "SetFontsFolder" لتعيين دليل سيعمل كمصدر خطوط جديد.
# مرر "false" كقيمة للمعامل "recursive" لتضمين الخطوط من جميع ملفات الخطوط الموجودة في الدليل
# الذي نمرره في المعامل الأول، ولكن لا تشمل أي خطوط في أي من المجلدات الفرعية لهذا الدليل.
# مرر "true" كقيمة للمعامل "recursive" لتضمين جميع ملفات الخطوط في الدليل الذي نمرره
# في المعامل الأول، بالإضافة إلى جميع الخطوط في مجلداته الفرعية.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# خط "Amethysta" موجود في مجلد فرعي داخل دليل الخطوط.
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# استعادة مصادر الخطوط الأصلية.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

