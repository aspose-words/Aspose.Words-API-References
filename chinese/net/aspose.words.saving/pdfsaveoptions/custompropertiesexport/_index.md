---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions CustomPropertiesExport 属性如何通过控制 CustomDocumentProperties 来增强您的 PDF 导出以获得最佳结果。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

获取或设置确定方式的值[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/)导出为 PDF 文件。

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## 评论

默认值为None。

Metadata保存为 PDF/A 时不支持该值。 Standard将用于 PDF/A-1 和 PDF/A-2 and None适用于 PDF/A-4。

Standard保存为 PDF 2.0 时不支持该值。 Metadata将被使用。

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
