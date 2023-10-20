---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: 用于 .NET 的 Aspose.Words
description: ImageSaveOptions ThresholdForFloydSteinbergDithering 财产. 获取或设置阈值该阈值确定 FloydSteinberg 方法中二值化误差的值  当ImageBinarizationMethod是FloydSteinbergDithering 在 C#.
type: docs
weight: 160
url: /zh/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

获取或设置阈值，该阈值确定 Floyd-Steinberg 方法中二值化误差的值 。 当[`ImageBinarizationMethod`](../../imagebinarizationmethod/)是FloydSteinbergDithering.

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## 评论

默认值为 128。

## 例子

演示如何在使用 Floyd-Steinberg 方法渲染 TIFF 图像时设置 TIFF 二值化错误阈值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为 TIFF 时，我们可以将 SaveOptions 对象传递给
// 调整 Aspose.Words 在渲染此图像时将应用的抖动。
// “ThresholdForFloydSteinbergDithering”属性的默认值为 128。
// 较高的值往往会产生较暗的图像。
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
