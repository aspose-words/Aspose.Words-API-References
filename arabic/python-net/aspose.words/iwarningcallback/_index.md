---
title: IWarningCallback class
linktitle: IWarningCallback class
articleTitle: IWarningCallback class
second_title: Aspose.Words for Python
description: "aspose.words.IWarningCallback class. Implement this interface if you want to have your own custom method called to  capture loss of fidelity warnings that can occur during document loading or saving."
type: docs
weight: 620
url: /ar/python-net/aspose.words/iwarningcallback/
---

## IWarningCallback class

Implement this interface if you want to have your own custom method called to 
capture loss of fidelity warnings that can occur during document loading or saving.


### Methods

| Name | Description |
| --- | --- |
|[ warning(info)](./warning/#warninginfo) | Aspose.Words invokes this method when it encounters some issue during document loading  or saving that might result in loss of formatting or data fidelity. |

### Examples

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
callback = self.FontSubstitutionWarningCollector()
doc.warning_callback = callback
# احفظ مجموعة مصادر الخطوط الحالية، والتي ستكون مصدر الخط الافتراضي لكل مستند.
# التي لا نحدد لها مصدر خط مختلف.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# لأغراض الاختبار، سنضبط Aspose.Words للبحث عن الخطوط فقط في مجلد غير موجود.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# عند عرض المستند، لن يكون هناك مكان للعثور على خط "Times New Roman".
# سيتسبب هذا في تحذير استبدال الخط، والذي سيكتشفه رد النداء الخاص بنا.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخط لدينا.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# عيّن رد اتصال لمعالجة تحذيرات استبدال الخط.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# حدد اسم خط افتراضي وفعل استبدال الخط.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# يجب استخدام مقاييس الخط الأصلية بعد استبدال الخط.
doc.layout_options.keep_original_font_metrics = True
# سنتلقى تحذير استبدال الخط إذا حفظنا مستندًا بخط مفقود.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings (FontSubstitutionWarningCollector).

```python
class FontSubstitutionWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
            self.font_substitution_warnings.warning(info)
```

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with image.docx')
metafile_rendering_options = aw.saving.MetafileRenderingOptions()
# اضبط خاصية "EmulateRasterOperations" إلى "false" للعودة إلى الصورة النقطية عندما
# يواجه ملفًا ميتا، مما سيتطلب عمليات نقطية للتصوير في ملف PDF الناتج.
metafile_rendering_options.emulate_raster_operations = False
# اضبط خاصية "RenderingMode" إلى "VectorWithFallback" لمحاولة عرض كل ملف ميتا باستخدام الرسومات المتجهة.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF وتطبيق الإعدادات
# في كائن MetafileRenderingOptions الخاص بنا لعملية الحفظ.
save_options = aw.saving.PdfSaveOptions()
save_options.metafile_rendering_options = metafile_rendering_options
callback = self.HandleDocumentWarnings()
doc.warning_callback = callback
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HandleBinaryRasterWarnings.pdf', save_options=save_options)
self.assertEqual(1, callback.warnings.count)
self.assertEqual("'R2_XORPEN' binary raster operation is not supported.", callback.warnings[0].description)
```

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records (HandleDocumentWarnings).

```python
class HandleDocumentWarnings(aw.IWarningCallback):

    def __init__(self):
        self.warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.MINOR_FORMATTING_LOSS:
            print('Unsupported operation: ' + info.description)
            self.warnings.warning(info)
```

### See Also

* module [aspose.words](../)

