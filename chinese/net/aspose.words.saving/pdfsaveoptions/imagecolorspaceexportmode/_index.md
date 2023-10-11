---
title: PdfSaveOptions.ImageColorSpaceExportMode
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 指定如何为 PDF 文档中的图像选择色彩空间
type: docs
weight: 190
url: /zh/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

指定如何为 PDF 文档中的图像选择色彩空间。

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

### 评论

默认值为Auto.

如果SimpleCmyk值已指定， [`ImageCompression`](../imagecompression/)选项被忽略并且 Flate 压缩用于文档中的所有图像。

SimpleCmyk保存为 PDF/A 时不支持该值。 Auto将使用值来代替。

### 例子

演示将文档导出为 PDF 时如何为文档中的图像设置不同的色彩空间。

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

// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.Auto”以获取Aspose.Words
// 自动选择转换为 PDF 的文档中图像的色彩空间。
// 在大多数情况下，颜色空间为 RGB。
// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.SimpleCmyk”
// 对保存的 PDF 中的所有图像使用 CMYK 色彩空间。
// Aspose.Words 还将对所有图像应用 Flate 压缩并忽略“ImageCompression”属性的值。
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### 也可以看看

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


