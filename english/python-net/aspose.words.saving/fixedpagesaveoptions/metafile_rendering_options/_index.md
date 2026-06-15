---
title: FixedPageSaveOptions.metafile_rendering_options property
linktitle: metafile_rendering_options property
articleTitle: metafile_rendering_options property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.metafile_rendering_options property. Allows to specify metafile rendering options."
type: docs
weight: 30
url: /python-net/aspose.words.saving/fixedpagesaveoptions/metafile_rendering_options/
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
# Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
# it encounters a metafile, which will require raster operations to render in the output PDF.
metafile_rendering_options.emulate_raster_operations = False
# Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF and applies the configuration
# in our MetafileRenderingOptions object to the saving operation.
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

