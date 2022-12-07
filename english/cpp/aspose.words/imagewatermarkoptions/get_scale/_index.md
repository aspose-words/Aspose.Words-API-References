---
title: get_Scale
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.
type: docs
weight: 40
url: /cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Remarks


Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

## Examples



Shows how to create a watermark from an image in the local file system. 
```cpp
auto doc = MakeObject<Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = MakeObject<ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"), imageWatermarkOptions);

doc->Save(ArtifactsDir + u"Document.ImageWatermark.docx");
```

## See Also

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
