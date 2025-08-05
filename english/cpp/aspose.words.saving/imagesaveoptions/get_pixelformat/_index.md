---
title: Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat method
linktitle: get_PixelFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat method. Gets or sets the pixel format for the generated images in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.saving/imagesaveoptions/get_pixelformat/
---
## ImageSaveOptions::get_PixelFormat method


Gets or sets the pixel format for the generated images.

```cpp
Aspose::Words::Saving::ImagePixelFormat Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat() const
```

## Remarks


This property has effect only when saving to raster image formats.

The default value is [Format32BppArgb](../../imagepixelformat/).

Pixel format of the output image may differ from the set value because of work of GDI+.

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

* Enum [ImagePixelFormat](../../imagepixelformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
