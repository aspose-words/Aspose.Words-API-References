---
title: ImageSaveOptions.metafile_rendering_options property
linktitle: metafile_rendering_options property
articleTitle: metafile_rendering_options property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.metafile_rendering_options property. Allows to specify how metafiles are treated in the rendered output."
type: docs
weight: 80
url: /zh/python-net/aspose.words.saving/imagesaveoptions/metafile_rendering_options/
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
# 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象来
# 确定保存操作将如何处理文档中的 Windows 元文件。
# 如果我们将 "RenderingMode" 属性设置为 "MetafileRenderingMode.Vector",
# 或 "MetafileRenderingMode.VectorWithFallback"，我们将把所有元文件渲染为矢量图形。
# 如果我们将 "RenderingMode" 属性设置为 "MetafileRenderingMode.Bitmap"，我们将把所有元文件渲染为位图。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
options.metafile_rendering_options.rendering_mode = metafile_rendering_mode
# 当值设置为 true 时，Aspose.Words 使用 GDI+ 来模拟光栅操作。
options.metafile_rendering_options.use_gdi_raster_operations_emulation = True
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.WindowsMetaFile.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

