---
title: Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution method
linktitle: get_HorizontalResolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution method. Gets or sets the horizontal resolution for the generated images, in dots per inch in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/imagesaveoptions/get_horizontalresolution/
---
## ImageSaveOptions::get_HorizontalResolution method


Gets or sets the horizontal resolution for the generated images, in dots per inch.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution() const
```

## Remarks


This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

## Examples



Shows how to edit the image while Aspose.Words converts a document to one. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// We can adjust these properties to change the image's brightness and contrast.
// Both are on a 0-1 scale and are at 0.5 by default.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// We can adjust horizontal and vertical resolution with these properties.
// This will affect the dimensions of the image.
// The default value for these properties is 96.0, for a resolution of 96dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// We can scale the image using this property. The default value is 1.0, for scaling of 100%.
// We can use this property to negate any changes in image dimensions that changing the resolution would cause.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
