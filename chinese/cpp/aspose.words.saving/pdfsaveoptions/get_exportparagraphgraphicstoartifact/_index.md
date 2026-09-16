---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact 方法"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact 方法。获取或设置一个值，以确定段落图形是否应在 C++ 中标记为 artifact。"
type: docs
weight: 17500
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


获取或设置一个值，以确定段落图形是否应标记为工件。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## 备注


默认值为 **false**，段落图形（下划线、文字强调等）将在文档的逻辑结构中标记为 "Span"。

当值为 **true** 时，段落图形将标记为 "Artifact"。

当 [ExportDocumentStructure](../get_exportdocumentstructure/) 为 **false** 时，此值将被忽略。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
