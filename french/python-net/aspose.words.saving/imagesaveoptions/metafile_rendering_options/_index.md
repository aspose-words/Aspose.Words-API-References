---
title: ImageSaveOptions.metafile_rendering_options property
linktitle: metafile_rendering_options property
articleTitle: metafile_rendering_options property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.metafile_rendering_options property. Allows to specify how metafiles are treated in the rendered output."
type: docs
weight: 80
url: /fr/python-net/aspose.words.saving/imagesaveoptions/metafile_rendering_options/
---

## ImageSaveOptions.metafile_rendering_options property

Allows to specify how metafiles are treated in the rendered output.


```python
@property
def metafile_rendering_options(self) -> aspose.words.saving.MetafileRenderingOptions:
    ...

```

### Remarks

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
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf')
# Lorsque nous enregistrons le document en tant qu'image, nous pouvons passer un objet SaveOptions à
# déterminez comment l'opération d'enregistrement traitera les métafichiers Windows dans le document.
# Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Vector",
# ou "MetafileRenderingMode.VectorWithFallback", nous rendrons tous les métafichiers en tant que graphiques vectoriels.
# Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Bitmap", nous rendrons tous les métafichiers sous forme de bitmap.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
options.metafile_rendering_options.rendering_mode = metafile_rendering_mode
# Aspose.Words utilise GDI+ pour l'émulation des opérations raster, lorsque la valeur est définie sur true.
options.metafile_rendering_options.use_gdi_raster_operations_emulation = True
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.WindowsMetaFile.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

