---
title: FontSettings.set_fonts_folders method
linktitle: set_fonts_folders method
articleTitle: set_fonts_folders method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folders method. Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts."
type: docs
weight: 90
url: /ar/python-net/aspose.words.fonts/fontsettings/set_fonts_folders/
---

## set_fonts_folders(fonts_folders, recursive) {#strlist_bool}

Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```python
def set_fonts_folders(self, fonts_folders: List[str], recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| fonts_folders | List[str] | An array of folders that contain TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




### Examples

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# مصادر الخطوط لدينا لا تحتوي على الخط الذي استخدمناه للنص في هذا المستند.
# إذا استخدمنا إعدادات الخط هذه أثناء تصيير هذا المستند،
# ستطبق Aspose.Words خطًا احتياطيًا على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد موقعه.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# مصادر الخطوط الافتراضية تفتقد الخطين الذين نستخدمهما في هذا المستند.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# استخدم طريقة "SetFontsFolders" لإنشاء مصدر خط من كل دليل خط نمرره كالمعامل الأول.
# مرّر "false" كمعامل "recursive" لتضمين الخطوط من جميع ملفات الخط الموجودة في الأدلة.
# التي نمررها كالمعامل الأول، لكن لا تشمل أي خطوط من أي من المجلدات الفرعية للأدلة.
# مرّر "true" كمعامل "recursive" لتضمين جميع ملفات الخط في الأدلة التي نمررها.
# كالمعامل الأول، بالإضافة إلى جميع الخطوط في المجلدات الفرعية لها.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# المجلد "Junction" نفسه لا يحتوي على ملفات خطوط، لكنه يحتوي على مجلدات فرعية تحتوي عليها.
if recursive:
    self.assertEqual(11, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# استعادة مصادر الخطوط الأصلية.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

