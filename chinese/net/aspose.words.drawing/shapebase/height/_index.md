---
title: ShapeBase.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words for .NET
description: 探索 ShapeBase Height 属性，轻松调整形状容器的高度，增强项目的设计灵活性和精确度。
type: docs
weight: 210
url: /zh/net/aspose.words.drawing/shapebase/height/
---
## ShapeBase.Height property

获取或设置形状包含块的高度。

```csharp
public double Height { get; set; }
```

## 评论

对于顶级形状，该值以点为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

## 例子

展示如何插入浮动图像，并指定其位置和大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// 配置形状的“RelativeHorizontalPosition”属性来处理“Left”属性的值
// 作为形状与页面左侧的水平距离（以点为单位）。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// 将形状与页面左侧的水平距离设置为 100。
shape.Left = 100;

// 以类似的方式使用“RelativeVerticalPosition”属性将形状定位在页面顶部下方 80pt 处。
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// 设置形状的高度，它将自动缩放宽度以保留尺寸。
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// “Bottom”和“Right”属性包含图像的底部和右侧边缘。
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
