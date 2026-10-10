---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# Когда мы сохраняем документ в формат OOXML, мы можем создать объект OoxmlSaveOptions
# а затем передать его методу сохранения документа, чтобы изменить способ сохранения документа.
# Установите свойство "compression_level" в "CompressionLevel.MAXIMUM", чтобы применить самое сильное и самое медленное сжатие.
# Установите свойство "compression_level" в "CompressionLevel.NORMAL", чтобы применить
# стандартное сжатие, которое использует Aspose.Words при сохранении документов OOXML.
# Установите свойство "compression_level" в "CompressionLevel.FAST", чтобы применить более быстрое и более слабое сжатие.
# Установите свойство "compression_level" в "CompressionLevel.SUPER_FAST", чтобы применить
# стандартное сжатие, которое использует Microsoft Word.
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

