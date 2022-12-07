---
title: get_UseHighQualityRendering
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.
type: docs
weight: 274
url: /cpp/aspose.words.saving/saveoptions/get_usehighqualityrendering/
---
## SaveOptions::get_UseHighQualityRendering method


Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering() const
```

## Remarks


The default value is **false**.

This property is used when the document is exported to image formats: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/).

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
