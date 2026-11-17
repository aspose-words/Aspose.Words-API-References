---
title: Aspose::Words::Saving::MetafileRenderingOptions::set_UseGdiRasterOperationsEmulation method
linktitle: set_UseGdiRasterOperationsEmulation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::set_UseGdiRasterOperationsEmulation method. Sets a value determining whether or not to use the GDI+ for raster operations emulation in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.saving/metafilerenderingoptions/set_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::set_UseGdiRasterOperationsEmulation method


Sets a value determining whether or not to use the GDI+ for raster operations emulation.

```cpp
void Aspose::Words::Saving::MetafileRenderingOptions::set_UseGdiRasterOperationsEmulation(bool value)
```

## Remarks


Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to **true**, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to **false**, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is **false**.
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
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
