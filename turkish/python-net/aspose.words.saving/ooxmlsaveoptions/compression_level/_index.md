---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /tr/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# Belgeyi OOXML formatında kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
# ve ardından belgeyi kaydetme yöntemine geçirerek belgeyi nasıl kaydettiğimizi değiştirebiliriz.
# "compression_level" özelliğini "CompressionLevel.MAXIMUM" olarak ayarlayarak en güçlü ve en yavaş sıkıştırmayı uygulayın.
# "compression_level" özelliğini "CompressionLevel.NORMAL" olarak ayarlayarak uygulayın
# Aspose.Words'ün OOXML belgelerini kaydederken kullandığı varsayılan sıkıştırma.
# "compression_level" özelliğini "CompressionLevel.FAST" olarak ayarlayarak daha hızlı ve daha zayıf bir sıkıştırma uygulayın.
# "compression_level" özelliğini "CompressionLevel.SUPER_FAST" olarak ayarlayarak uygulayın
# Microsoft Word'ün kullandığı varsayılan sıkıştırma.
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

