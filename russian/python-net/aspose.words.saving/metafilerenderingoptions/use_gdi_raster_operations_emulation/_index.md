---
title: MetafileRenderingOptions.use_gdi_raster_operations_emulation property
linktitle: use_gdi_raster_operations_emulation property
articleTitle: use_gdi_raster_operations_emulation property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_gdi_raster_operations_emulation property. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 80
url: /ru/python-net/aspose.words.saving/metafilerenderingoptions/use_gdi_raster_operations_emulation/
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
* class [MetafileRenderingOptions](../)

