---
title: CompressionLevel enumeration
linktitle: CompressionLevel enumeration
articleTitle: CompressionLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.CompressionLevel enumeration. Compression level for OOXML and XPS files"
type: docs
weight: 30
url: /sv/python-net/aspose.words.saving/compressionlevel/
---

## CompressionLevel enumeration

Compression level for OOXML and XPS files.
(DOCX, DOTX and XPS files are internally a ZIP-archive, this property controls the compression level of the archive.

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

Shows how to control the compression level when saving a document to XPS format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Sample document for XPS compression test.')
# Skapa ett XpsSaveOptions object och ställ in komprimeringsnivån.
options = aw.saving.XpsSaveOptions()
options.compression_level = aw.saving.CompressionLevel.MAXIMUM
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.CompressionLevelXps.xps', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

