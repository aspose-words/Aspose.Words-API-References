---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream 方法"
linktitle: "get_ImageStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream 方法。允许指定图像将在 C++ 中保存到的流。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


允许指定图像将要保存的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## 备注


此属性允许您在 HTML 期间将图像保存到流而不是文件。

默认值为 **null**。当此属性为 **null** 时，图像将保存到在 [ImageFileName](../get_imagefilename/) 属性中指定的文件。

使用 [IImageSavingCallback](../../iimagesavingcallback/) 时，您不能用另一张图像替换图像。它仅用于控制图像保存位置。

## 另见

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
