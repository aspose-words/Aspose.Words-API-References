---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions UseGdiRasterOperationsEmulation property. Gets or sets a value determining whether or not to use the GDI for raster operations emulation in C#.
type: docs
weight: 80
url: /net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Remarks

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to `true`, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to `false`, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is `false`.

## Examples

Shows how to set the rendering mode when saving documents with Windows Metafile images to other image formats.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// When we save the document as an image, we can pass a SaveOptions object to
// determine how the saving operation will process Windows Metafiles in the document.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
// or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### See Also

* class [MetafileRenderingOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
