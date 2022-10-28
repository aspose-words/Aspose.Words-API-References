---
title: get_PixelFormat
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the pixel format for the generated images.
type: docs
weight: 131
url: /cpp/aspose.words.saving/imagesaveoptions/get_pixelformat/
---
## ImageSaveOptions.get_PixelFormat method


Gets or sets the pixel format for the generated images.

```cpp
Aspose::Words::Saving::ImagePixelFormat Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat() const
```


This property has effect only when saving to raster image formats.

The default value is **Format32BppArgb**.

Pixel format of the output image may differ from the set value because of work of GDI+.

## Examples




Shows how to select a bit-per-pixel rate with which to render a document to an image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

ASSERT_LT(20000, MakeObject<System::IO::FileInfo>(ImageDir + u"Logo.jpg")->get_Length());

// When we save the document as an image, we can pass a SaveOptions object to
// select a pixel format for the image that the saving operation will generate.
// Various bit per pixel rates will affect the quality and file size of the generated image.
auto imageSaveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Png);
imageSaveOptions->set_PixelFormat(imagePixelFormat);

// We can clone ImageSaveOptions instances.
ASPOSE_ASSERT_NE(imageSaveOptions, imageSaveOptions->Clone());

doc->Save(ArtifactsDir + u"ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

