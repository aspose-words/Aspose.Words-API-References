---
title: Aspose::Words::Saving::ImageSaveOptions::get_ImageSize method
linktitle: get_ImageSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_ImageSize method. Gets or sets the size of a generated image in pixels in C++.'
type: docs
weight: 7500
url: /cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Gets or sets the size of a generated image in pixels.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Remarks


This property has effect only when saving to raster image formats.

The default value is (0 x 0), which means that the size of the generated image will be calculated according to the size of the image in points, the specified resolution and scale.

## Examples



Shows how to render every page of a document to a separate TIFF image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Set the "PageSet" property to the number of the first page from
    // which to start rendering the document from.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Export page at 2325x5325 pixels and 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
