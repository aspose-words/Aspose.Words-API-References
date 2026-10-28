---
title: Aspose::Words::ImageWatermarkOptions::set_Scale method
linktitle: set_Scale
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImageWatermarkOptions::set_Scale method. Sets the scale factor expressed as a fraction of the image. The default value is 0 - auto in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/imagewatermarkoptions/set_scale/
---
## ImageWatermarkOptions::set_Scale method


Sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

```cpp
void Aspose::Words::ImageWatermarkOptions::set_Scale(double value)
```

## Remarks


Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.
## Examples


Shows how to create a watermark from an image in the local file system.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// We have a different options to insert image.
// Use on of the following methods to add image watermark.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);


doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```
## Exceptions

* **ArgumentOutOfRangeException** -  Throws when argument was out of the range of valid values.

## See Also

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
