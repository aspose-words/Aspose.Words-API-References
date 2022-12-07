---
title: get_UseAntiAliasing
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to use anti-aliasing for rendering.
type: docs
weight: 261
url: /cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Gets or sets a value determining whether or not to use anti-aliasing for rendering.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Remarks


The default value is **false**. When this value is set to **true** anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). When the document is exported to the [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) and [Azw3](../../../aspose.words/saveformat/) formats this option is used for raster images.

## Examples



Shows how to improve the quality of a rendered document with [SaveOptions](../). 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

SharedPtr<SaveOptions> options = MakeObject<Aspose::Words::Saving::ImageSaveOptions>(SaveFormat::Jpeg);

doc->Save(ArtifactsDir + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(ArtifactsDir + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
