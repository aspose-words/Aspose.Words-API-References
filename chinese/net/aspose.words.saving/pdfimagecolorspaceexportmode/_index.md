---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode 枚举. 指定如何为 PDF 文档中的图像选择色彩空间 在 C#.
type: docs
weight: 5480
url: /zh/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

指定如何为 PDF 文档中的图像选择色彩空间。

```csharp
public enum PdfImageColorSpaceExportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | Aspose.Words 自动为每张图像选择最合适的色彩空间。 |
| SimpleCmyk | `1` | Aspose.Words 使用简单的公式将 RGB 图像转换为 CMYK 颜色空间。 |

## 例子

展示了在我们将文档导出为 PDF 时如何为文档中的图像设置不同的色彩空间。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.Auto”以获取 Aspose.Words
// 自动为转换为 PDF 的文档中的图像选择色彩空间。
// 在大多数情况下，颜色空间将是 RGB。
// 将“ImageColorSpaceExportMode”属性设置为“PdfImageColorSpaceExportMode.SimpleCmyk”
// 为保存的 PDF 中的所有图像使用 CMYK 颜色空间。
// Aspose.Words 还将对所有图像应用 Flate 压缩并忽略“ImageCompression”属性的值。
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
