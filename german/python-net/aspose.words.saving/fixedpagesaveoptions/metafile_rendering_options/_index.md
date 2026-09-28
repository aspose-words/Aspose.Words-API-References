---
title: FixedPageSaveOptions.metafile_rendering_options property
linktitle: metafile_rendering_options property
articleTitle: metafile_rendering_options property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.metafile_rendering_options property. Allows to specify metafile rendering options."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/fixedpagesaveoptions/metafile_rendering_options/
---

## FixedPageSaveOptions.metafile_rendering_options property

Allows to specify metafile rendering options.


```python
@property
def metafile_rendering_options(self) -> aspose.words.saving.MetafileRenderingOptions:
    ...

@metafile_rendering_options.setter
def metafile_rendering_options(self, value: aspose.words.saving.MetafileRenderingOptions):
    ...

```

### Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with image.docx')
metafile_rendering_options = aw.saving.MetafileRenderingOptions()
# Setzen Sie die Eigenschaft "EmulateRasterOperations" auf "false", um im Falle eines Rückfalls zu Bitmap zu verwenden, wenn
# es eine Metadatei trifft, die Rasteroperationen zum Rendern im Ausgabe‑PDF erfordert.
metafile_rendering_options.emulate_raster_operations = False
# Setzen Sie die Eigenschaft "RenderingMode" auf "VectorWithFallback", um zu versuchen, jede Metadatei mit Vektorgrafiken zu rendern.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert und die Konfiguration anwendet
# in unserem MetafileRenderingOptions‑Objekt für den Speicher‑Vorgang.
save_options = aw.saving.PdfSaveOptions()
save_options.metafile_rendering_options = metafile_rendering_options
callback = self.HandleDocumentWarnings()
doc.warning_callback = callback
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HandleBinaryRasterWarnings.pdf', save_options=save_options)
self.assertEqual(1, callback.warnings.count)
self.assertEqual("'R2_XORPEN' binary raster operation is not supported.", callback.warnings[0].description)
```

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records (HandleDocumentWarnings).

```python
class HandleDocumentWarnings(aw.IWarningCallback):

    def __init__(self):
        self.warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.MINOR_FORMATTING_LOSS:
            print('Unsupported operation: ' + info.description)
            self.warnings.warning(info)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

