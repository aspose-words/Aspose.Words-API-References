---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ImageBinarizationMethod 枚举，实现高效的图像二值化。使用先进的技术优化您的文档处理。
type: docs
weight: 5950
url: /zh/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

指定用于二值化图像的方法。

```csharp
public enum ImageBinarizationMethod
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Threshold | `0` | 指定阈值方法。 |
| FloydSteinbergDithering | `1` | 指定使用 Floyd-Steinberg 误差扩散方法进行抖动。 |

## 例子

展示如何在使用 Floyd-Steinberg 方法渲染 TIFF 图像时设置 TIFF 二值化错误阈值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为 TIFF 时，我们可以将 SaveOptions 对象传递给
// 调整 Aspose.Words 在渲染此图像时将应用的抖动。
// “ThresholdForFloydSteinbergDithering”属性的默认值为128。
// 值越高，图像就越暗。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
