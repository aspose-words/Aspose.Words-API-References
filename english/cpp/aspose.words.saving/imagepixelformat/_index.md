---
title: ImagePixelFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the pixel format for the generated images of document pages.
type: docs
weight: 833
url: /cpp/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enum


Specifies the pixel format for the generated images of document pages.

```cpp
enum class ImagePixelFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Format16BppRgb555 | 0 | 16 bits per pixel, RGB. |
| Format16BppRgb565 | 1 | 16 bits per pixel, RGB. |
| Format16BppArgb1555 | 2 | 16 bits per pixel, ARGB. |
| Format24BppRgb | 3 | 24 bits per pixel, RGB. |
| Format32BppRgb | 4 | 32 bits per pixel, RGB. |
| Format32BppArgb | 5 | 32 bits per pixel, ARGB. |
| Format32BppPArgb | 6 | 32 bits per pixel, ARGB, premultiplied alpha. |
| Format48BppRgb | 7 | 48 bits per pixel, RGB. |
| Format64BppArgb | 8 | 64 bits per pixel, ARGB. |
| Format64BppPArgb | 9 | 64 bits per pixel, ARGB, premultiplied alpha. |
| Format1bppIndexed | 10 | 1 bit per pixel, Indexed. |


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

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
