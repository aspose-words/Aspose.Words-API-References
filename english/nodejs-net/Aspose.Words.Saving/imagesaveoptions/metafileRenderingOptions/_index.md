---
title: ImageSaveOptions.metafileRenderingOptions property
linktitle: metafileRenderingOptions property
articleTitle: metafileRenderingOptions property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.metafileRenderingOptions property. Allows to specify how metafiles are treated in the rendered output."
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/imagesaveoptions/metafileRenderingOptions/
---

## ImageSaveOptions.metafileRenderingOptions property

Allows to specify how metafiles are treated in the rendered output.


```js
get metafileRenderingOptions(): Aspose.Words.Saving.MetafileRenderingOptions
```

### Remarks

When [MetafileRenderingMode.Vector](../../metafilerenderingmode/#Vector) is specified, Aspose.Words renders
metafile to vector graphics using its own metafile rendering engine first and then renders vector
graphics to the image.

When [MetafileRenderingMode.Bitmap](../../metafilerenderingmode/#Bitmap) is specified, Aspose.Words renders
metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low
resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text)
on the page. Aspose.Words metafile rendering engine will produce more consistent result even
on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../metafilerenderingmode/) is [MetafileRenderingMode.Bitmap](../../metafilerenderingmode/#Bitmap).




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
* class [ImageSaveOptions](../)

