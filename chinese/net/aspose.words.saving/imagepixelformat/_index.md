---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.ImagePixelFormat 枚举，以获得文档页面图像的最佳像素格式。轻松增强文档视觉效果！
type: docs
weight: 5970
url: /zh/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

指定生成的文档页面图像的像素格式。

```csharp
public enum ImagePixelFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 每像素 16 位，RGB。 |
| Format16BppRgb565 | `1` | 每像素 16 位，RGB。 |
| Format16BppArgb1555 | `2` | 每像素 16 位，ARGB。 |
| Format24BppRgb | `3` | 每像素 24 位，RGB。 |
| Format32BppRgb | `4` | 每像素 32 位，RGB。 |
| Format32BppArgb | `5` | 每像素 32 位，ARGB。 |
| Format32BppPArgb | `6` | 每像素 32 位，ARGB，预乘 alpha。 |
| Format48BppRgb | `7` | 每像素 48 位，RGB。 |
| Format64BppArgb | `8` | 每像素 64 位，ARGB。 |
| Format64BppPArgb | `9` | 每像素 64 位，ARGB，预乘 alpha。 |
| Format1bppIndexed | `10` | 每像素 1 位，索引。 |

## 例子

展示如何选择将文档渲染为图像的每像素位数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 为保存操作将生成的图像选择像素格式。
// 不同的每像素比特率将影响生成图像的质量和文件大小。
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// 我们可以克隆 ImageSaveOptions 实例。
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
