---
title: OoxmlSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/ooxmlsaveoptions/compression_level/
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
# Wenn wir das Dokument in ein OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
# und es dann an die Speicher‑Methode des Dokuments übergeben, um zu ändern, wie wir das Dokument speichern.
# Setzen Sie die "compression_level"-Eigenschaft auf "CompressionLevel.MAXIMUM", um die stärkste und langsamste Kompression anzuwenden.
# Setzen Sie die "compression_level"-Eigenschaft auf "CompressionLevel.NORMAL", um anzuwenden
# die Standardkompression, die Aspose.Words beim Speichern von OOXML-Dokumenten verwendet.
# Setzen Sie die "compression_level"-Eigenschaft auf "CompressionLevel.FAST", um eine schnellere und schwächere Kompression anzuwenden.
# Setzen Sie die "compression_level"-Eigenschaft auf "CompressionLevel.SUPER_FAST", um anzuwenden
# die Standardkompression, die Microsoft Word verwendet.
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

