---
title: MetafileRenderingOptions.use_gdi_raster_operations_emulation property
linktitle: use_gdi_raster_operations_emulation property
articleTitle: use_gdi_raster_operations_emulation property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_gdi_raster_operations_emulation property. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 80
url: /it/python-net/aspose.words.saving/metafilerenderingoptions/use_gdi_raster_operations_emulation/
---

## MetafileRenderingOptions.use_gdi_raster_operations_emulation property

Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation.


```python
@property
def use_gdi_raster_operations_emulation(self) -> bool:
    ...

@use_gdi_raster_operations_emulation.setter
def use_gdi_raster_operations_emulation(self, value: bool):
    ...

```

### Remarks

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation
comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to ``True``, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to ``False``, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is ``False``.




### Examples

Shows how to set the rendering mode when saving documents with Windows Metafile images to other image formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf')
# Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
# determina come l'operazione di salvataggio elaborerà i Metafile di Windows nel documento.
# Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Vector",
# oppure "MetafileRenderingMode.VectorWithFallback", renderizzeremo tutti i metafile come grafica vettoriale.
# Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Bitmap", renderizzeremo tutti i metafile come bitmap.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
options.metafile_rendering_options.rendering_mode = metafile_rendering_mode
# Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster, quando il valore è impostato su true.
options.metafile_rendering_options.use_gdi_raster_operations_emulation = True
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.WindowsMetaFile.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

