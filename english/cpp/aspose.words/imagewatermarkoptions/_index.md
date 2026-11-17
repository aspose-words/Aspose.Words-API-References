---
title: Aspose::Words::ImageWatermarkOptions class
linktitle: ImageWatermarkOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImageWatermarkOptions class. Contains options that can be specified when adding a watermark with image. To learn more, visit the  documentation article in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Contains options that can be specified when adding a watermark with image. To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) documentation article.

```cpp
class ImageWatermarkOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is **true**. |
| [get_Scale](./get_scale/)() const | Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Setter for [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Setter for [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

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

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
