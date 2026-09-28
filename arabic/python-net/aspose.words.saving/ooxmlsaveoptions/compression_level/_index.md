---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
---

## OoxmlSaveOptions.compression_level property

Specifies the compression level used to save document.
The default value is [CompressionLevel.NORMAL](../../compressionlevel/#NORMAL).



```python
@property
def compression_level(self) -> aspose.words.saving.CompressionLevel:
    ...

@compression_level.setter
def compression_level(self, value: aspose.words.saving.CompressionLevel):
    ...

```

### Examples

Shows how to specify the compression level to use while saving an OOXML document.

```python
doc = aw.Document(MY_DIR + 'Big document.docx')
# عند حفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
# ثم نمرره إلى طريقة حفظ المستند لتعديل طريقة حفظ المستند.
# اضبط خاصية "compression_level" إلى "CompressionLevel.MAXIMUM" لتطبيق أقوى وأبطأ ضغط.
# اضبط خاصية "compression_level" إلى "CompressionLevel.NORMAL" لتطبيق
# الضغط الافتراضي الذي يستخدمه Aspose.Words عند حفظ مستندات OOXML.
# اضبط خاصية "compression_level" إلى "CompressionLevel.FAST" لتطبيق ضغط أسرع وأضعف.
# اضبط خاصية "compression_level" إلى "CompressionLevel.SUPER_FAST" لتطبيق
# الضغط الافتراضي الذي يستخدمه Microsoft Word.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compression_level = compression_level
start_time = time.perf_counter()
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.document_compression.docx', save_options)
elapsed_ms = 1000 * (time.perf_counter() - start_time)
file_size = os.path.getsize(ARTIFACTS_DIR + 'OoxmlSaveOptions.document_compression.docx')
print(f'Saving operation done using the "{compression_level}" compression level:')
print(f'\tDuration:\t{elapsed_ms} ms')
print(f'\tFile Size:\t{file_size} bytes')
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

