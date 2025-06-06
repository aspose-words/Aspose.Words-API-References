---
title: ImageData.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words for .NET
description: 探索 ImageData ImageSize 属性，轻松访问有关图像尺寸和分辨率的基本细节，以增强视觉质量。
type: docs
weight: 130
url: /zh/net/aspose.words.drawing/imagedata/imagesize/
---
## ImageData.ImageSize property

获取有关图像大小和分辨率的信息。

```csharp
public ImageSize ImageSize { get; }
```

## 评论

如果图像仅链接而未存储在文档中，则返回零大小。

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

* class [ImageSize](../../imagesize/)
* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
