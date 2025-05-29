---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions ImageColorSpaceExportMode 属性，以优化 PDF 中的图像颜色选择，从而获得令人惊叹的视觉质量和一致性。
type: docs
weight: 190
url: /zh/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

指定如何为 PDF 文档中的图像选择颜色空间。

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## 评论

默认值为Auto.

如果SimpleCmyk指定值， [`ImageCompression`](../imagecompression/)选项被忽略并且 Flate 压缩用于文档中的所有图像。

SimpleCmyk保存为 PDF/A 时不支持该值。 Auto值将被使用。

## 例子

展示如何在将文档导出为 PDF 时为文档中的图像设置不同的颜色空间。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.Auto”以使 Aspose.Words
// 自动选择转换为 PDF 的文档中图像的颜色空间。
// 大多数情况下，颜色空间将是 RGB。
// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.SimpleCmyk”
// 对保存的 PDF 中的所有图像使用 CMYK 颜色空间。
// Aspose.Words 还将对所有图像应用 Flate 压缩并忽略“ImageCompression”属性的值。
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### 也可以看看

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
