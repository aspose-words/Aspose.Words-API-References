---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /ar/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# أنشئ كائن "RtfSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمستند لتعديل طريقة حفظه كملف RTF.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# عيّن الخاصية "ExportCompactSize" إلى "true" لت
# تقليل حجم المستند المحفوظ على حساب توافق النص من اليمين إلى اليسار.
options.export_compact_size = True
# عيّن الخاصية "ExportImagesFotOldReaders" إلى "true" لاستخدام كلمات مفتاحية إضافية لضمان أن مستندنا هو
# متوافق مع قارئات ما قبل Microsoft Word 97 وWordPad.
# عيّن الخاصية "ExportImagesFotOldReaders" إلى "false" لتقليل حجم المستند،
# ولكن يمنع القارئات القديمة من القدرة على قراءة أي صور غير ميتافايل أو BMP قد يحتويها المستند.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

