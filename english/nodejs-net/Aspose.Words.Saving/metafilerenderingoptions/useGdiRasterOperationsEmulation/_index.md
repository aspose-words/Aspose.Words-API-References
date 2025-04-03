---
title: MetafileRenderingOptions.useGdiRasterOperationsEmulation property
linktitle: useGdiRasterOperationsEmulation property
articleTitle: useGdiRasterOperationsEmulation property
second_title: Aspose.Words for NodeJs
description: "MetafileRenderingOptions.useGdiRasterOperationsEmulation property. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Saving/metafilerenderingoptions/useGdiRasterOperationsEmulation/
---

## MetafileRenderingOptions.useGdiRasterOperationsEmulation property

Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation.


```js
get useGdiRasterOperationsEmulation(): boolean
```

### Remarks

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation
comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to ``true``, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to ``false``, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is ``false``.




### Examples

Shows how to set the rendering mode when saving documents with Windows Metafile images to other image formats.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertImage(base.imageDir + "Windows MetaFile.wmf");

// When we save the document as an image, we can pass a SaveOptions object to
// determine how the saving operation will process Windows Metafiles in the document.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
// or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);
options.metafileRenderingOptions.renderingMode = metafileRenderingMode;
// Aspose.words uses GDI+ for raster operations emulation, when value is set to true.
options.metafileRenderingOptions.useGdiRasterOperationsEmulation = true;

doc.save(base.artifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MetafileRenderingOptions](../)

