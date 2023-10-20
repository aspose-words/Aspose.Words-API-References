---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions JpegQuality 财产. 获取或设置确定 PDF 文档中 JPEG 图像质量的值 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

获取或设置确定 PDF 文档中 JPEG 图像质量的值。

```csharp
public int JpegQuality { get; set; }
```

## 评论

默认值为 100。

此属性与[`ImageCompression`](../imagecompression/)选项。

仅当文档包含 JPEG 图像时才有效。

以 PDF 格式保存时，使用此属性获取或设置文档中图像的质量。 值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。 如果质量是 100 并且源图像是 JPEG，这意味着没有压缩 - 原始字节将被保存。

## 例子

演示如何为我们要转换为 PDF 的文档中的所有图像指定压缩类型。

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

// 将“ImageCompression”属性设置为“PdfImageCompression.Auto”以使用
// “ImageCompression” 属性来控制最终在输出 PDF 中的 Jpeg 图像的质量。
// 将“ImageCompression”属性设置为“PdfImageCompression.Jpeg”以使用
// “ImageCompression” 属性来控制最终在输出 PDF 中的所有图像的质量。
pdfSaveOptions.ImageCompression = pdfImageCompression;

// 将“JpegQuality”属性设置为“10”，以牺牲图像质量为代价加强压缩。
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
