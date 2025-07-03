---
title: Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod method
linktitle: get_TiffBinarizationMethod
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod method. Gets or sets method used while converting images to 1 bpp format when SaveFormat is Tiff and TiffCompression is equal to Ccitt3 or Ccitt4 in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Gets or sets method used while converting images to 1 bpp format when [SaveFormat](../get_saveformat/) is [Tiff](../../../aspose.words/saveformat/) and [TiffCompression](../get_tiffcompression/) is equal to [Ccitt3](../../tiffcompression/) or [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Remarks


The default value is [Threshold](../../imagebinarizationmethod/).

## Examples



Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// When we save the document as a TIFF, we can pass a SaveOptions object to
// adjust the dithering that Aspose.Words will apply when rendering this image.
// The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
// Higher values tend to produce darker images.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## See Also

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
