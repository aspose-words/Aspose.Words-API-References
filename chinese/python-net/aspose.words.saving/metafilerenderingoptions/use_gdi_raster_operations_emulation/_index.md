---
title: MetafileRenderingOptions.use_gdi_raster_operations_emulation property
linktitle: use_gdi_raster_operations_emulation property
articleTitle: use_gdi_raster_operations_emulation property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_gdi_raster_operations_emulation property. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 80
url: /zh/python-net/aspose.words.saving/metafilerenderingoptions/use_gdi_raster_operations_emulation/
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
* class [MetafileRenderingOptions](../)

