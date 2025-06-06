---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ImageSize 类，它是您获取详细图像大小和分辨率见解的首选资源，可帮助您提高文档质量。
type: docs
weight: 1400
url: /zh/net/aspose.words.drawing/imagesize/
---
## ImageSize class

包含有关图像大小和分辨率的信息。

要了解更多信息，请访问[处理图像](https://docs.aspose.com/words/net/working-with-images/)文档文章。

```csharp
public class ImageSize
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | 将宽度和高度初始化为给定的像素值。将分辨率初始化为 96 dpi。 |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | 将宽度、高度和分辨率初始化为给定值。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | 获取图像的高度（以像素为单位）。 |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | 获取图像的高度（以点为单位）。1 点为 1/72 英寸。 |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | 获取 DPI 中的水平分辨率。 |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | 获取 DPI 中的垂直分辨率。 |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | 获取图像的宽度（以像素为单位）。 |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | 获取图像的宽度（以点为单位）。1 点为 1/72 英寸。 |

## 例子

展示如何使用图像调整形状的大小。

```csharp
// 当我们使用“InsertImage”方法插入图像时，构建器会缩放显示图像的形状，以便
// 当我们在 Microsoft Word 中使用 100% 缩放查看文档时，形状会以实际大小显示图像。
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// 400x400 的图像将创建一个图像大小为 300x300pt 的 ImageData 对象。
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// 如果形状的尺寸与图像数据的尺寸相匹配，
// 然后形状以原始大小显示图像。
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // 将形状的整体尺寸缩小 50%。
shape.Width *= 0.5;

 // 缩放因子同时应用于宽度和高度以保持形状的比例。
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// 当我们调整形状大小时，图像数据的大小保持不变。
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// 我们可以参考图像数据尺寸来根据图像的大小进行缩放。
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### 也可以看看

* property [ImageSize](../imagedata/imagesize/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
