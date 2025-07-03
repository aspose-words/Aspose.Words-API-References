---
title: Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing method
linktitle: get_UseAntiAliasing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing method. Gets or sets a value determining whether or not to use anti-aliasing for rendering in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Gets or sets a value determining whether or not to use anti-aliasing for rendering.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Remarks


The default value is **false**. When this value is set to **true** anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). When the document is exported to the [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) or [Mobi](../../../aspose.words/saveformat/) formats this option is used for raster images.

## Examples



Shows how to improve the quality of a rendered document with [SaveOptions](../). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
