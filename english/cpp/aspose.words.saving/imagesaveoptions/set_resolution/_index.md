---
title: Aspose::Words::Saving::ImageSaveOptions::set_Resolution method
linktitle: set_Resolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::set_Resolution method. Sets both horizontal and vertical resolution for the generated images, in dots per inch in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Sets both horizontal and vertical resolution for the generated images, in dots per inch.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Remarks


This property has effect only when saving to raster image formats.

## Examples



Shows how to specify a resolution while rendering a document to PNG. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(ImageDir + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Png);

// Set the "Resolution" property to "72" to render the document in 72dpi.
options->set_Resolution(72.0f);

doc->Save(ArtifactsDir + u"ImageSaveOptions.Resolution.72dpi.png", options);

ASSERT_GE(120000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.Resolution.72dpi.png")->get_Length());

// Set the "Resolution" property to "300" to render the document in 300dpi.
options->set_Resolution(300.0f);

doc->Save(ArtifactsDir + u"ImageSaveOptions.Resolution.300dpi.png", options);

ASSERT_LT(700000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.Resolution.300dpi.png")->get_Length());
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
