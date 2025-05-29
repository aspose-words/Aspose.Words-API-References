---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.PdfCustomPropertiesExport 枚举如何通过自定义文档属性来增强 PDF 导出以获得最佳结果。
type: docs
weight: 6210
url: /zh/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

指定方式[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/)导出为 PDF 文件。

```csharp
public enum PdfCustomPropertiesExport
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 未导出任何自定义属性。 |
| Standard | `1` | 自定义属性将作为 /Info 字典中的条目导出。 |
| Metadata | `2` | 自定义属性是元数据。 |

## 例子

展示如何在将文档转换为 PDF 时导出自定义属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.None”以丢弃
// 当我们将文档保存为 .PDF 时自定义文档属性。
// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.Standard”
// 在输出 PDF 文档中保留自定义属性。
// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.Metadata”
// 在 XMP 包中保存自定义属性。
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
