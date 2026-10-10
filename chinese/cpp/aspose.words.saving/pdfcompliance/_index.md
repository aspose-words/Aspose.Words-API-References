---
title: "Aspose::Words::Saving::PdfCompliance enum"
linktitle: "PdfCompliance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfCompliance 枚举。指定 C++ 中的 PDF 标准合规级别。"
type: docs
weight: 73000
url: /zh/cpp/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enum


指定 PDF 标准合规级别。

```cpp
enum class PdfCompliance
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Pdf17 | 0 | 输出文件将符合 PDF 1.7（ISO 32000-1）标准。 |
| Pdf20 | 1 | 输出文件将符合 PDF 2.0（ISO 32000-2）标准。 |
| PdfA1a | 2 | 输出文件将符合 PDF/A-1a（ISO 19005-1）标准。此级别包括 PDF/A-1b 的所有要求，并额外要求包含文档结构（也称为 "标记"），其目的是确保文档内容可被搜索和重新利用。 |
| PdfA1b | 3 | 输出文件将符合 PDF/A-1b（ISO 19005-1）标准。PDF/A-1b 的目标是确保文档视觉外观的可靠再现。 |
| PdfA2a | 4 | 输出文件将符合 PDF/A-2a（ISO 19005-2）标准。此级别包括 PDF/A-2u 的所有要求，并额外要求包含文档结构（也称为 "标记"），其目的是确保文档内容可被搜索和重新利用。 |
| PdfA2u | 5 | 输出文件将符合 PDF/A-2u（ISO 19005-2）标准。PDF/A-2u 的目标是保持文档随时间的静态视觉外观，独立于创建、存储或渲染文件的工具和系统。此外，文档中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。 |
| PdfA3a | 6 | 输出文件将符合 PDF/A-3a（ISO 19005-3）标准。此级别包括 PDF/A-3u 的所有要求，并额外要求包含文档结构（也称为 "标记"），其目的是确保文档内容可被搜索和重新利用。 |
| PdfA3u | 7 | 输出文件将符合 PDF/A-3u（ISO 19005-3）标准。PDF/A-3u（以及 PDF/A-2u）旨在保持文档随时间的静态视觉外观，独立于创建、存储或渲染文件的工具和系统。此外，文档中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。除了 PDF/A-2u，PDF/A-3u 还允许将附件嵌入 PDF 文档。 |
| PdfA4 | 8 | 输出文件将符合 PDF/A-4（ISO 19005-4:2020）标准。PDF/A-4 的目标是保持文档随时间的静态视觉外观，独立于创建、存储或渲染文件的工具和系统。此外，文档中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。 |
| PdfA4f | 9 | 输出文件将符合 PDF/A-4f（ISO 19005-4:2020）标准。此级别包括 PDF/A-4 的所有要求，并额外允许将附件嵌入 PDF 文档。 |
| PdfA4Ua2 | 10 | 输出文件将符合 PDF/A-4 (ISO 19005-4:2020) 和 PDF/UA-2 (ISO 14289-2:2024) 两项标准。PDF/A-4 的目标是随着时间的推移保持文档的静态视觉外观，独立于用于创建、存储或呈现文件的工具和系统。PDF/UA 的主要目的是定义如何以一种使文件可访问的方式在 PDF 格式中表示电子文档。 |
| PdfUa1 | 11 | 输出文件将符合 PDF/UA-1 (ISO 14289-1) 标准。PDF/UA 的主要目的是定义如何以一种使文件可访问的方式在 PDF 格式中表示电子文档。 |
| PdfUa2 | 12 | 输出文件将符合 PDF/UA-2 (ISO 14289-2:2024) 标准。PDF/UA 的主要目的是定义如何以一种使文件可访问的方式在 PDF 格式中表示电子文档。 |

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
