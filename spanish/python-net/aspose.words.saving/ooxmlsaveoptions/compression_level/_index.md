---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /es/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# Al guardar el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
# y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
# Establezca la propiedad "compression_level" a "CompressionLevel.MAXIMUM" para aplicar la compresión más fuerte y lenta.
# Establezca la propiedad "compression_level" a "CompressionLevel.NORMAL" para aplicar
# la compresión predeterminada que Aspose.Words usa al guardar documentos OOXML.
# Establezca la propiedad "compression_level" a "CompressionLevel.FAST" para aplicar una compresión más rápida y débil.
# Establezca la propiedad "compression_level" a "CompressionLevel.SUPER_FAST" para aplicar
# la compresión predeterminada que usa Microsoft Word.
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

