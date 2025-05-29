---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 的 JpegQuality 属性优化您的 PDF 图像，让您可以控制 JPEG 质量以获得令人惊叹的文档视觉效果。
type: docs
weight: 220
url: /zh/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

获取或设置确定 PDF 文档内 JPEG 图像质量的值。

```csharp
public int JpegQuality { get; set; }
```

## 评论

默认值为 100。

此属性与[`ImageCompression`](../imagecompression/)选项。

仅当文档包含 JPEG 图像时才有效。

使用此属性可在以 PDF 格式保存时获取或设置文档内图像的质量。 值的范围是 0 到 100，其中 0 表示质量最差但压缩率最大，100 表示质量最好但压缩率最小。 如果质量为 100 且源图像为 JPEG，则表示不压缩 - 将保存原始字节。

## 例子

展示如何为要转换为 PDF 的文档中的所有图像指定压缩类型。

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
// 将“ImageCompression”属性设置为“PdfImageCompression.Auto”以使用
// “ImageCompression”属性用于控制最终输出 PDF 中的 Jpeg 图像的质量。
// 将“ImageCompression”属性设置为“PdfImageCompression.Jpeg”以使用
//“ImageCompression”属性用于控制最终输出 PDF 中所有图像的质量。
pdfSaveOptions.ImageCompression = pdfImageCompression;
// 将“JpegQuality”属性设置为“10”以加强压缩，但牺牲图像质量。
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
