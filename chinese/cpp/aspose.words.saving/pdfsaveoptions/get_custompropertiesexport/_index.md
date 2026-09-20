---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport 方法"
linktitle: "get_CustomPropertiesExport"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport 方法。获取或设置决定 CustomDocumentProperties 导出到 PDF 文件方式的值，在 C++ 中。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_custompropertiesexport/
---
## PdfSaveOptions::get_CustomPropertiesExport method


获取或设置决定 [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) 导出到 PDF 文件方式的值。

```cpp
Aspose::Words::Saving::PdfCustomPropertiesExport Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport() const
```

## 备注


默认值是 [None](../../pdfcustompropertiesexport/)。

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead. 
## 另见

* Enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
