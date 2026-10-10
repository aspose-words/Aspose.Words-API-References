---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations 方法"
linktitle: "get_EmulateRasterOperations"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations 方法。获取或设置决定在 C++ 中是否应仿真光栅操作的值。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


获取或设置决定是否应模拟光栅操作的值。

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## 备注


元文件中可能使用特定的光栅操作。它们无法直接渲染为矢量图形。仿真光栅操作需要对生成的矢量图形进行部分光栅化，这可能影响元文件的渲染性能。

当此值设置为 **true** 时，Aspose.Words 仿真光栅操作。生成的输出可能部分光栅化，性能可能会变慢。

当此值设置为 **false** 时，Aspose.Words 不仿真光栅操作。当 [Aspose.Words](../../../aspose.words/) 在元文件中遇到光栅操作时，它会回退到使用操作系统将元文件渲染为位图。

此选项仅在元文件被渲染为矢量图形时使用。

默认值为 **true**。
## 另见

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
