---
title: "Aspose::Words::Saving::DownsampleOptions 类"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DownsampleOptions 类。允许指定下采样选项。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


允许指定下采样选项。欲了解更多，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class DownsampleOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | 指定是否应对图像进行下采样。 |
| [get_Resolution](./get_resolution/)() const | 指定图像应下采样到的分辨率（每英寸像素）。 |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | 指定阈值分辨率（每英寸像素）。如果文档中图像的分辨率低于阈值，则不会应用下采样算法。值为 0 表示不使用阈值检查，所有可以减小尺寸的图像都会被下采样。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | 指定是否应对图像进行下采样。 |
| [set_Resolution](./set_resolution/)(int32_t) | 指定图像应下采样到的分辨率（每英寸像素）。 |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | 用于设置 [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/)。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
