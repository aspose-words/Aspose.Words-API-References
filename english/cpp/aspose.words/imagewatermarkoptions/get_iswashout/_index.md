---
title: get_IsWashout
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is True.
type: docs
weight: 14
url: /cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is True.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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
