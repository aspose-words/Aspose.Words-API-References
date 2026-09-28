---
title: FontSettings.get_fonts_sources method
linktitle: get_fonts_sources method
articleTitle: get_fonts_sources method
second_title: Aspose.Words for Python
description: "FontSettings.get_fonts_sources method. Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts."
type: docs
weight: 50
url: /ar/python-net/aspose.words.fonts/fontsettings/get_fonts_sources/
---

## get_fonts_sources() {#default}

Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.


```python
def get_fonts_sources(self):
    ...
```

### Remarks

The returned value is a copy of the data that Aspose.Words uses. If you change the entries
in the returned array, it will have no effect on document rendering. To specify new font sources
use the [FontSettings.set_fonts_sources()](../set_fonts_sources/#fontsourcebaselist) method.




### Returns

A copy of the current font sources.


### Examples

Shows how to add a font source to our existing font sources.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# مصدر الخط الافتراضي يفتقد إلى خطين نستخدمهما في مستندنا.
# عند حفظ هذا المستند، سيقوم Aspose.Words بتطبيق خطوط احتياطية على جميع النصوص المنسقة بخطوط غير قابلة للوصول.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# أنشئ مصدر خط من مجلد يحتوي على خطوط.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
# طبق مصفوفة جديدة من مصادر الخط التي تحتوي على مصادر الخط الأصلية، بالإضافة إلى خطوطنا المخصصة.
updated_font_sources = [original_font_sources[0], folder_font_source]
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=updated_font_sources)
# تحقق من أن Aspose.Words يمتلك الوصول إلى جميع الخطوط المطلوبة قبل أن نقوم بتحويل المستند إلى PDF.
updated_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in updated_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in updated_font_sources[1].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Junction Light' for f in updated_font_sources[1].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.AddFontSource.pdf')
# استعادة مصادر الخطوط الأصلية.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

