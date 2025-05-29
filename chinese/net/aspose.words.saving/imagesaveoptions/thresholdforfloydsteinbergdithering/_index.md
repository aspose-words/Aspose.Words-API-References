---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words for .NET
description: 使用 Floyd-Steinberg 抖动算法的 ImageSaveOptions Threshold 来优化您的图像。控制二值化误差，获得更佳的图像处理效果。
type: docs
weight: 160
url: /zh/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

获取或设置确定 Floyd-Steinberg 方法中的二值化误差值的阈值。 当[`ImageBinarizationMethod`](../../imagebinarizationmethod/)是FloydSteinbergDithering.

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## 评论

默认值为 128。

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

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
