---
title: Aspose::Words::Saving::TiffCompression enum
linktitle: TiffCompression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TiffCompression enum. Specifies what type of compression to apply when saving page images into a TIFF file in C++.'
type: docs
weight: 85000
url: /cpp/aspose.words.saving/tiffcompression/
---
## TiffCompression enum


Specifies what type of compression to apply when saving page images into a TIFF file.

```cpp
enum class TiffCompression
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Specifies no compression. |
| Rle | 1 | Specifies the RLE compression scheme. |
| Lzw | 2 | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| Ccitt3 | 3 | Specifies the CCITT3 compression scheme. |
| Ccitt4 | 4 | Specifies the CCITT4 compression scheme. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
