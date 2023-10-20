---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: 用于 .NET 的 Aspose.Words
description: ImageSize HeightPoints 财产. 获取图像的高度以磅为单位 1 点是 1/72 英寸 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

获取图像的高度（以磅为单位）。 1 点是 1/72 英寸。

```csharp
public double HeightPoints { get; }
```

## 例子

显示如何使用图像调整形状的大小。

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // 当我们使用“InsertImage”方法插入图像时，构建器会缩放显示图像的形状，以便，
            // 当我们在 Microsoft Word 中使用 100% 缩放查看文档时，形状会以其实际大小显示图像。
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // 一个 400x400 的图像将创建一个图像大小为 300x300pt 的 ImageData 对象。
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // 如果形状的尺寸与图像数据的尺寸匹配，
            // 然后形状会以其原始大小显示图像。
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // 将形状的整体尺寸减小 50%。
            shape.Width *= 0.5;

             // 缩放因子同时应用于宽度和高度，以保持形状的比例。
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // 当我们调整形状大小时，图像数据的大小保持不变。
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // 我们可以参考图像数据尺寸来根据图像大小应用缩放。
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### 也可以看看

* class [ImageSize](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
