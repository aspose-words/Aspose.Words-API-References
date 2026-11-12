---
title: ImageSaveOptions.metafile_rendering_options property
linktitle: metafile_rendering_options property
articleTitle: metafile_rendering_options property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.metafile_rendering_options property. Allows to specify how metafiles are treated in the rendered output."
type: docs
weight: 80
url: /ru/python-net/aspose.words.saving/imagesaveoptions/metafile_rendering_options/
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
# При сохранении документа в виде изображения мы можем передать объект SaveOptions к
# определите, как операция сохранения будет обрабатывать Windows Metafile в документе.
# Если мы установим свойство "RenderingMode" в значение "MetafileRenderingMode.Vector",
# или "MetafileRenderingMode.VectorWithFallback", мы будем рендерить все метафайлы как векторную графику.
# Если мы установим свойство "RenderingMode" в значение "MetafileRenderingMode.Bitmap", мы будем рендерить все метафайлы как растровые изображения.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
options.metafile_rendering_options.rendering_mode = metafile_rendering_mode
# Aspose.Words использует GDI+ для эмуляции растровых операций, когда значение установлено в true.
options.metafile_rendering_options.use_gdi_raster_operations_emulation = True
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.WindowsMetaFile.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

