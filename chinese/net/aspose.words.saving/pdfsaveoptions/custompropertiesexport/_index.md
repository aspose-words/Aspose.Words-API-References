---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 获取或设置一个确定方式的值CustomDocumentProperties导出为 PDF 文件
type: docs
weight: 50
url: /zh/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

获取或设置一个确定方式的值[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/)导出为 PDF 文件。

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### 评论

默认值为None.

Metadata保存为 PDF/A 时不支持该值。 Standard将用于 PDF/A-1 和 PDF/A-2 and None对于 PDF/A-4。

Standard保存为 PDF 2.0. 时不支持该值Metadata将被使用。

### 例子

显示如何在将文档转换为 PDF 时导出自定义属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.None”以丢弃
// 我们将文档保存为 .PDF 时的自定义文档属性。
// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.Standard”
// 在输出 PDF 文档中保留自定义属性。
// 将“CustomPropertiesExport”属性设置为“PdfCustomPropertiesExport.Metadata”
// 在 XMP 数据包中保留自定义属性。
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### 也可以看看

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


