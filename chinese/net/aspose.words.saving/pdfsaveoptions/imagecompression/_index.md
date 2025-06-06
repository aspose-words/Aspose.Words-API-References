---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 的 ImageCompression 属性优化您的 PDF，让您可以为生动的高质量图像选择最佳的压缩类型。
type: docs
weight: 200
url: /zh/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

指定文档中所有图像使用的压缩类型。

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## 评论

默认为Auto。

使用Jpeg让您通过以下方式控制输出文档中的图像质量[`JpegQuality`](../jpegquality/)财产。

使用Jpeg与其他压缩类型的性能相比，它提供了最快的转换速度， 但在这种情况下，存在有损 JPEG 压缩。

使用Auto通过以下方式控制输出文档中的 Jpeg 质量[`JpegQuality`](../jpegquality/)属性， 但对于其他格式，原始像素数据被提取并使用 Flate 压缩保存。 这种情况比 Jpeg 转换慢但无损。

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
