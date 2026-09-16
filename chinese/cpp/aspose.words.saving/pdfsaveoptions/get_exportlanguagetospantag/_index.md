---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag 方法"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag 方法。获取或设置一个值，以确定是否在 C++ 中的文档结构中创建 \"Span\" 标记来导出文本语言。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


获取或设置一个值，以确定是否在文档结构中创建 "Span" 标签来导出文本语言。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## 备注


默认值为 **false**，并且 "Lang" 属性附加到页面内容流中的标记内容序列。

当值为 **true** 时，会为非默认语言的文本创建 "Span" 标记，并将 "Lang" 属性附加到该标记上。

当 [ExportDocumentStructure](../get_exportdocumentstructure/) 为 **false** 时，此值将被忽略。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
