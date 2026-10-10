---
title: "Aspose::Words::Saving::PdfCustomPropertiesExport 枚举"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfCustomPropertiesExport 枚举。指定在 C++ 中 CustomDocumentProperties 导出到 PDF 文件的方式。"
type: docs
weight: 74000
url: /zh/cpp/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enum


指定 [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) 导出到 PDF 文件的方式。

```cpp
enum class PdfCustomPropertiesExport
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 未导出任何自定义属性。 |
| 标准 | 1 | 自定义属性作为 /Info 字典中的条目导出。以下名称的自定义属性不导出：“Title”、“Author”、“Subject”、“Keywords”、“Creator”、“Producer”、“CreationDate”、“ModDate”、“Trapped”。 |
| 元数据 | 2 | 自定义属性是元数据。 |

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
