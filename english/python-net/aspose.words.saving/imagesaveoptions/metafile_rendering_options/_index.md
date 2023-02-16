---
title: metafile_rendering_options property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify how metafiles are treated in the rendered output."
type: docs
weight: 70
url: /python-net/aspose.words.saving/imagesaveoptions/metafile_rendering_options/
---

## ImageSaveOptions.metafile_rendering_options property

Allows to specify how metafiles are treated in the rendered output.

When [MetafileRenderingMode.VECTOR](../../metafilerenderingmode/#VECTOR) is specified, Aspose.Words renders
metafile to vector graphics using its own metafile rendering engine first and then renders vector
graphics to the image.

When [MetafileRenderingMode.BITMAP](../../metafilerenderingmode/#BITMAP) is specified, Aspose.Words renders
metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low
resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text)
on the page. Aspose.Words metafile rendering engine will produce more consistent result even
on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../metafilerenderingmode/) is [MetafileRenderingMode.BITMAP](../../metafilerenderingmode/#BITMAP).




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
* class [ImageSaveOptions](../)

