---
title: Aspose::Words::ImageWatermarkOptions::get_IsWashout method
linktitle: get_IsWashout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImageWatermarkOptions::get_IsWashout method. Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is true in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
