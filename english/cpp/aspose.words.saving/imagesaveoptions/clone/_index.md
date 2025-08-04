---
title: Aspose::Words::Saving::ImageSaveOptions::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::Clone method. Creates a deep clone of this object in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions::Clone method


Creates a deep clone of this object.

```cpp
System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> Aspose::Words::Saving::ImageSaveOptions::Clone()
```


## Examples



Shows how to select a bit-per-pixel rate with which to render a document to an image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a pixel format for the image that the saving operation will generate.
// Various bit per pixel rates will affect the quality and file size of the generated image.
auto imageSaveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
imageSaveOptions->set_PixelFormat(imagePixelFormat);

// We can clone ImageSaveOptions instances.
ASPOSE_ASSERT_NE(imageSaveOptions, imageSaveOptions->Clone());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

## See Also

* Class [ImageSaveOptions](../)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
