---
title: get_TiffCompression
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the type of compression to apply when saving generated images to the TIFF format.
type: docs
weight: 209
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertImage(ImageDir + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);

// Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
// which may result in a very large output file.
// Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
// Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
// Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
options->set_TiffCompression(tiffCompression);

doc->Save(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff", options);

switch (tiffCompression)
{
case TiffCompression::None:
    ASSERT_LT(3000000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff")->get_Length());
    break;

case TiffCompression::Rle:
    ASSERT_LT(600000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff")->get_Length());
    break;

case TiffCompression::Lzw:
    ASSERT_LT(200000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff")->get_Length());
    break;

case TiffCompression::Ccitt3:
    ASSERT_GE(90000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff")->get_Length());
    break;

case TiffCompression::Ccitt4:
    ASSERT_GE(20000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.TiffImageCompression.tiff")->get_Length());
    break;
}
```

## See Also

* Enum [TiffCompression](../../tiffcompression/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
