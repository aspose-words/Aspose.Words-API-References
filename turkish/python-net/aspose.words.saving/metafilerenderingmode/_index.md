---
title: MetafileRenderingMode enumeration
linktitle: MetafileRenderingMode enumeration
articleTitle: MetafileRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MetafileRenderingMode enumeration. Specifies how Aspose.Words should render WMF and EMF metafiles."
type: docs
weight: 490
url: /tr/python-net/aspose.words.saving/metafilerenderingmode/
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
# "EmulateRasterOperations" özelliğini "false" olarak ayarlayın, bitmap'e geri dönmek için karşılaşıldığında
# bir metafile ile karşılaştığında, çıktıda PDF olarak renderlemek için raster işlemleri gerekecektir.
metafile_rendering_options.emulate_raster_operations = False
# "RenderingMode" özelliğini "VectorWithFallback" olarak ayarlayın, her metafile'ı vektör grafikleriyle renderlemeyi denemek için.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu metodun belgeyi .PDF'ye nasıl dönüştürdüğünü ve yapılandırmayı nasıl uyguladığını değiştirmek için
# kaydetme işlemi sırasında MetafileRenderingOptions nesnemizde.
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

