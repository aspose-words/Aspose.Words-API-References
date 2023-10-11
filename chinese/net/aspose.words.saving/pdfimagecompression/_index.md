---
title: Enum PdfImageCompression
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.PdfImageCompression 枚举. 指定应用于 PDF 文件中的图像的压缩类型
type: docs
weight: 5490
url: /zh/net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

指定应用于 PDF 文件中的图像的压缩类型。

```csharp
public enum PdfImageCompression
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | 自动为每个图像选择最合适的压缩。 |
| Jpeg | `1` | Jpeg 压缩。 不支持透明度。 |

### 例子

演示如何为我们要转换为 PDF 的文档中的所有图像指定压缩类型。

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
// “ImageCompression”属性控制最终输出 PDF 中的所有图像的质量。
pdfSaveOptions.ImageCompression = pdfImageCompression;

// 将“JpegQuality”属性设置为“10”以牺牲图像质量为代价加强压缩。
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


