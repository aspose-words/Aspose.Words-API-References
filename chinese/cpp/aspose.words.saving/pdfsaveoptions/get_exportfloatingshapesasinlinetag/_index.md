---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag 方法"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag 方法。获取或设置一个值，以确定在 C++ 中是否将浮动形状导出为文档结构中的内联标签。"
type: docs
weight: 16500
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


获取或设置一个值，以确定浮动形状是否以内联标签的形式导出到文档结构中。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## 备注


默认值为 **false**，浮动形状将导出为块级标签，放置在其锚定的段落之后。

当值为 **true** 时，浮动形状将导出为内联标签，放置在其锚定的段落内部。

当 [ExportDocumentStructure](../get_exportdocumentstructure/) 为 **false** 时，此值将被忽略。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
