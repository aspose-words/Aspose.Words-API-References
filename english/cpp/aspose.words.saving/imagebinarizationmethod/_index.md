---
title: ImageBinarizationMethod
second_title: Aspose.Words for C++ API Reference
description: Specifies the method used to binarize image.
type: docs
weight: 807
url: /cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Specifies the method used to binarize image.

```cpp
enum class ImageBinarizationMethod
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Threshold | 0 | Specifies threshold method. |
| FloydSteinbergDithering | 1 | Specifies dithering using Floyd-Steinberg error diffusion method. |


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

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
