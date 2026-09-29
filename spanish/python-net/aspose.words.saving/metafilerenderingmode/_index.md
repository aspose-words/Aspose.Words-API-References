---
title: MetafileRenderingMode enumeration
linktitle: MetafileRenderingMode enumeration
articleTitle: MetafileRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MetafileRenderingMode enumeration. Specifies how Aspose.Words should render WMF and EMF metafiles."
type: docs
weight: 490
url: /es/python-net/aspose.words.saving/metafilerenderingmode/
---

## MetafileRenderingMode enumeration

Specifies how Aspose.Words should render WMF and EMF metafiles.


### Members

| Name | Description |
| --- | --- |
| VECTOR_WITH_FALLBACK | Aspose.Words tries to render a metafile as vector graphics. If Aspose.Words cannot correctly render some of  the metafile records to vector graphics then Aspose.Words renders this metafile to a bitmap. |
| VECTOR | Aspose.Words renders a metafile as vector graphics. |
| BITMAP | Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document. |

### Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with image.docx')
metafile_rendering_options = aw.saving.MetafileRenderingOptions()
# Establezca la propiedad "EmulateRasterOperations" a "false" para volver a bitmap cuando
# encuentre un metafile, lo que requerirá operaciones raster para renderizar en el PDF de salida.
metafile_rendering_options.emulate_raster_operations = False
# Establezca la propiedad "RenderingMode" a "VectorWithFallback" para intentar renderizar cada metafile usando gráficos vectoriales.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF y aplica la configuración
# en nuestro objeto MetafileRenderingOptions a la operación de guardado.
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

* module [aspose.words.saving](../)

