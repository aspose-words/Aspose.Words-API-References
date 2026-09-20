---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream method"
linktitle: "get_CssStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream 方法。允许指定在 C++ 中保存 CSS 信息的流。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


允许指定 CSS 信息将被保存到的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## 备注


此属性允许您将 CSS 信息保存到流中。

默认值为 **null**。此属性不会抑制将 CSS 信息保存到文件或嵌入到 HTML 文档。要抑制导出 CSS，请使用 [IsExportNeeded](../get_isexportneeded/) 属性。

使用 [ICssSavingCallback](../../icsssavingcallback/) 时，您不能用其他内容替代 CSS。它仅用于将 CSS 保存到流中。

## 另见

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
