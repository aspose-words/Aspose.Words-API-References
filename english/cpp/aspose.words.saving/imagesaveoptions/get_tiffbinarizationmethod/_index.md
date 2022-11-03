---
title: get_TiffBinarizationMethod
second_title: Aspose.Words for C++ API Reference
description: Gets or sets method used while converting images to 1 bpp format when SaveFormat is SaveFormat.Tiff and TiffCompression is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4.
type: docs
weight: 183
url: /cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions.get_TiffBinarizationMethod method


Gets or sets method used while converting images to 1 bpp format when [SaveFormat](../get_saveformat/) is **SaveFormat.Tiff** and [TiffCompression](../get_tiffcompression/) is equal to **TiffCompression.Ccitt3** or **TiffCompression.Ccitt4**.

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```


The default value is **ImageBinarizationMethod.Threshold**.

## Examples




Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

// When we save the document as a TIFF, we can pass a SaveOptions object to
// adjust the dithering that Aspose.Words will apply when rendering this image.
// The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
// Higher values tend to produce darker images.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);
options->set_TiffCompression(TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(ArtifactsDir + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```
