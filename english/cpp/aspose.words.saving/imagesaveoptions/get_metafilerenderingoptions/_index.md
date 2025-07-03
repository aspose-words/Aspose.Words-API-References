---
title: Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions method
linktitle: get_MetafileRenderingOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions method. Allows to specify how metafiles are treated in the rendered output in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Allows to specify how metafiles are treated in the rendered output.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Remarks


When [Vector](../../metafilerenderingmode/) is specified, Aspose.Words renders metafile to vector graphics using its own metafile rendering engine first and then renders vector graphics to the image.

When [Bitmap](../../metafilerenderingmode/) is specified, Aspose.Words renders metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text) on the page. Aspose.Words metafile rendering engine will produce more consistent result even on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../metafilerenderingmode/) is [Bitmap](../../metafilerenderingmode/).

## Examples



Shows how to set the rendering mode when saving documents with Windows Metafile images to other image formats. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// When we save the document as an image, we can pass a SaveOptions object to
// determine how the saving operation will process Windows Metafiles in the document.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
// or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
// If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## See Also

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
