---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages 方法"
linktitle: "get_PreblendImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages 方法。获取或设置一个值，以确定在 C++ 中是否对透明图像进行与黑色背景色的预混合。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


获取或设置一个值，以确定是否将透明图像与黑色背景颜色预先混合。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## 备注


对图像进行预混合可能会提升 PDF 文档在 Adobe Reader 中的视觉效果，并消除抗锯齿伪影。

为了正确显示预混合图像，PDF 查看器应用程序必须支持软遮罩图像字典中的 /Matte 条目。此外，预混合图像可能会降低 PDF 渲染性能。

默认值为 **false**。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
