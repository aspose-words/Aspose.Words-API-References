---
title: MetafileRenderingOptions.use_gdi_raster_operations_emulation property
linktitle: use_gdi_raster_operations_emulation property
articleTitle: use_gdi_raster_operations_emulation property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_gdi_raster_operations_emulation property. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 80
url: /python-net/aspose.words.saving/metafilerenderingoptions/use_gdi_raster_operations_emulation/
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
builder = aw.DocumentBuilder(doc)

builder.insert_image(drawing.Image.from_file(IMAGE_DIR + "Windows MetaFile.wmf"))

# When we save the document as an image, we can pass a SaveOptions object to
# determine how the saving operation will process Windows Metafiles in the document.
# If we set the "rendering_mode" property to "MetafileRenderingMode.VECTOR",
# or "MetafileRenderingMode.VECTOR_WITH_FALLBACK", we will render all metafiles as vector graphics.
# If we set the "rendering_mode" property to "MetafileRenderingMode.BITMAP", we will render all metafiles as bitmaps.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
options.metafile_rendering_options.rendering_mode = metafile_rendering_mode
# Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
options.metafile_rendering_options.use_gdi_raster_operations_emulation = True

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.windows_meta_file.png", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

