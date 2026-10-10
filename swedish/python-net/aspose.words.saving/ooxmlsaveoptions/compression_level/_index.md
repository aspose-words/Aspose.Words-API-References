---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /sv/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# När vi sparar dokumentet till ett OOXML-format kan vi skapa ett OoxmlSaveOptions object
# och sedan skicka det till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
# Ställ in egenskapen "compression_level" till "CompressionLevel.MAXIMUM" för att tillämpa den starkaste och långsammaste komprimeringen.
# Ställ in egenskapen "compression_level" till "CompressionLevel.NORMAL" för att tillämpa
# standardkomprimeringen som Aspose.Words använder när OOXML-dokument sparas.
# Ställ in egenskapen "compression_level" till "CompressionLevel.FAST" för att tillämpa en snabbare och svagare komprimering.
# Ställ in egenskapen "compression_level" till "CompressionLevel.SUPER_FAST" för att tillämpa
# standardkomprimeringen som Microsoft Word använder.
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

