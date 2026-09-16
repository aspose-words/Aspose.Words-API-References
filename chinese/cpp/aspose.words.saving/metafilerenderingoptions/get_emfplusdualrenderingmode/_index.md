---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode 方法"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode 方法。获取或设置决定在 C++ 中如何渲染 EMF+ Dual 元文件的值。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


获取或设置决定 EMF+ Dual 元文件应如何渲染的值。

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## 备注


EMF+ Dual 元文件包含 EMF+ 和 EMF 两部分。MS Word 和 GDI+ 总是渲染 EMF+ 部分。Aspose.Words 目前尚未完全支持所有 EMF+ 记录，在某些情况下 EMF 部分的渲染结果看起来比 EMF+ 部分更好。

此选项仅在元文件被渲染为矢量图形时使用。当元文件渲染为位图时，始终使用 EMF+ 部分。

默认值是 [EmfPlusWithFallback](../../emfplusdualrenderingmode/)。
## 另见

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
