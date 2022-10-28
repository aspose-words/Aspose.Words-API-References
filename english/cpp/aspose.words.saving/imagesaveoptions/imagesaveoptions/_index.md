---
title: ImageSaveOptions
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of this class that can be used to save rendered images in the Tiff, Png, Bmp, Emf, Jpeg or Svg format. Png, Bmp, Jpeg or Svg format.
type: docs
weight: 1
url: /cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions.ImageSaveOptions method


Initializes a new instance of this class that can be used to save rendered images in the **Tiff**, **Png**, **Bmp**, **Emf**, **Jpeg** or **Svg** format. **Png**, **Bmp**, **Jpeg** or **Svg** format.

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Can be **Tiff**, **Png**, **Bmp**, **Emf**, **Jpeg** or **Svg**. **Png**, **Bmp**, **Jpeg** or **Svg**. |

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

