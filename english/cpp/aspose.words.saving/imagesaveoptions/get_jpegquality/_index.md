---
title: Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality method
linktitle: get_JpegQuality
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality method. Gets or sets a value determining the quality of the generated JPEG images in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/imagesaveoptions/get_jpegquality/
---
## ImageSaveOptions::get_JpegQuality method


Gets or sets a value determining the quality of the generated JPEG images.

```cpp
int32_t Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality()
```

## Remarks


Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

## Examples



Shows how to configure compression while saving a document as a JPEG. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertImage(ImageDir + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto imageOptions = MakeObject<ImageSaveOptions>(SaveFormat::Jpeg);

// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions->set_JpegQuality(10);

doc->Save(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

ASSERT_GE(20000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighCompression.jpg")->get_Length());

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions->set_JpegQuality(100);

doc->Save(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

ASSERT_LT(60000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighQuality.jpg")->get_Length());
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
