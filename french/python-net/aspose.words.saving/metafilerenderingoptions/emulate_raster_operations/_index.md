---
title: MetafileRenderingOptions.emulate_raster_operations property
linktitle: emulate_raster_operations property
articleTitle: emulate_raster_operations property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emulate_raster_operations property. Gets or sets a value determining whether or not the raster operations should be emulated."
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/metafilerenderingoptions/emulate_raster_operations/
---

## MetafileRenderingOptions.emulate_raster_operations property

Gets or sets a value determining whether or not the raster operations should be emulated.


```python
@property
def emulate_raster_operations(self) -> bool:
    ...

@emulate_raster_operations.setter
def emulate_raster_operations(self, value: bool):
    ...

```

### Remarks

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics.
Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the
metafile rendering performance.

When this value is set to ``True``, Aspose.Words emulates the raster operations. The resulting output maybe
partially rasterized and performance might be slower.

When this value is set to ``False``, Aspose.Words does not emulate the raster operations. When Aspose.Words
encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the
operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is ``True``.




### Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with image.docx')
metafile_rendering_options = aw.saving.MetafileRenderingOptions()
# Définissez la propriété "EmulateRasterOperations" sur "false" pour revenir au bitmap lorsque
# il rencontre un métafichier, ce qui nécessitera des opérations raster pour le rendre dans le PDF de sortie.
metafile_rendering_options.emulate_raster_operations = False
# Définissez la propriété "RenderingMode" sur "VectorWithFallback" pour tenter de rendre chaque métafichier en utilisant des graphiques vectoriels.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF et applique la configuration
# dans notre objet MetafileRenderingOptions lors de l'opération d'enregistrement.
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
* class [MetafileRenderingOptions](../)

