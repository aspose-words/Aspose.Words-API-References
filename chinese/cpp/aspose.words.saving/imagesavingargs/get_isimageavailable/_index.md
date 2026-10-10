---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable 方法"
linktitle: "get_IsImageAvailable"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable 方法。返回 true，如果当前图像可用于导出（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


如果当前图像可导出，则返回 **true**。

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## 备注


文档中的某些图像可能不可用，例如，因为图像是链接的且链接不可访问或未指向有效图像。在这种情况下，Aspose.Words 会导出带有红色叉的图标。此属性在原始图像可用时返回 **true**；在原始图像不可用时返回 **false**，并将在保存时提供一个 \"no image\" 图标。

在保存组形状或不需要任何图像的形状时，此属性始终为 **true**。

## 另见

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
