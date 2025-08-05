---
title: Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression method
linktitle: get_TiffCompression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression method. Gets or sets the type of compression to apply when saving generated images to the TIFF format in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.saving/imagesaveoptions/get_tiffcompression/
---
## ImageSaveOptions::get_TiffCompression method


Gets or sets the type of compression to apply when saving generated images to the TIFF format.

```cpp
Aspose::Words::Saving::TiffCompression Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression() const
```

## Remarks


Has effect only when saving to TIFF.

The default value is [Lzw](../../tiffcompression/).

## Examples



Shows how to select the compression scheme to apply to a document that we convert into a TIFF image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
// Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
// which may result in a very large output file.
// Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
// Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
options->set_TiffCompression(tiffCompression);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.TiffImageCompression.tiff", options);
```

## See Also

* Enum [TiffCompression](../../tiffcompression/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
