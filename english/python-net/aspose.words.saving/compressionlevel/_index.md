---
title: CompressionLevel enumeration
linktitle: CompressionLevel enumeration
articleTitle: CompressionLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.CompressionLevel enumeration. Compression level for OOXML files"
type: docs
weight: 30
url: /python-net/aspose.words.saving/compressionlevel/
---

## CompressionLevel enumeration

Compression level for OOXML files. 
(DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive.

Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)




### Members

| Name | Description |
| --- | --- |
| NORMAL | Normal compression level. Default compression level used by Aspose.Words. |
| MAXIMUM | Maximum compression level. |
| FAST | Fast compression level. |
| SUPER_FAST | Super Fast compression level. Microsoft Word uses this compression level. |

### Examples

Shows how to specify the compression level to use while saving an OOXML document.

```python
doc = aw.Document(MY_DIR + 'Big document.docx')
# When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
# and then pass it to the document's saving method to modify how we save the document.
# Set the "compression_level" property to "CompressionLevel.MAXIMUM" to apply the strongest and slowest compression.
# Set the "compression_level" property to "CompressionLevel.NORMAL" to apply
# the default compression that Aspose.Words uses while saving OOXML documents.
# Set the "compression_level" property to "CompressionLevel.FAST" to apply a faster and weaker compression.
# Set the "compression_level" property to "CompressionLevel.SUPER_FAST" to apply
# the default compression that Microsoft Word uses.
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

* module [aspose.words.saving](../)

