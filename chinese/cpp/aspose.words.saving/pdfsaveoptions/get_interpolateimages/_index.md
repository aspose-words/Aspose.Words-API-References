---
title: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages 方法"
linktitle: "get_InterpolateImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages 方法。一个标志，指示符合规范的阅读器是否应执行图像插值。当指定为 false 时，该标志不会写入输出文档，而是使用阅读器的默认行为，在 C++ 中。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


指示符合规范的阅读器是否应执行图像插值的标志。当指定 **false** 时，标志不会写入输出文档，而是使用阅读器的默认行为。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## 备注


当源图像的分辨率明显低于输出设备的分辨率时，每个源样本覆盖多个设备像素。因此，图像可能出现锯齿或块状。这些视觉伪影可以通过在渲染期间应用图像插值算法来减小。插值不是用相同的颜色为源样本覆盖的所有像素着色，而是尝试在相邻样本值之间产生平滑过渡。

符合规范的阅读器可能选择不实现此 PDF 功能，或使用其希望的任何特定插值实现。

默认值为 **false**。

PDF/A 合规性禁止使用插值标志。保存为 PDF/A 时将自动使用 **false** 值。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
