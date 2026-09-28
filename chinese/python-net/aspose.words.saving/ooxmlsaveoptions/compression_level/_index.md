---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
# 然后将其传递给文档的保存方法，以修改文档的保存方式。
# 将 "compression_level" 属性设置为 "CompressionLevel.MAXIMUM"，以应用最强且最慢的压缩。
# 将 "compression_level" 属性设置为 "CompressionLevel.NORMAL"，以应用
# Aspose.Words 在保存 OOXML 文档时使用的默认压缩。
# 将 "compression_level" 属性设置为 "CompressionLevel.FAST"，以应用更快且更弱的压缩。
# 将 "compression_level" 属性设置为 "CompressionLevel.SUPER_FAST"，以应用
# Microsoft Word 使用的默认压缩。
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

