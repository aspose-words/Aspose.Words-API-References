---
title: ShapeBase.AdjustWithEffects
linktitle: AdjustWithEffects
articleTitle: AdjustWithEffects
second_title: Aspose.Words for .NET
description: 了解 ShapeBase AdjustWithEffects 方法如何通过添加效果范围来增强源矩形，提供精确的最终矩形值。
type: docs
weight: 660
url: /zh/net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

将效果范围的源矩形值添加到并返回最终矩形。

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

## 例子

展示如何检查形状的边界如何受到形状效果的影响。

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// 这两个形状在尺寸和形状类型方面是相同的。
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// 第一个形状没有效果，第二个形状有阴影和粗轮廓。
// 这些效果使得第二个形状的轮廓尺寸大于第一个形状的轮廓尺寸。
// 尽管我们在 Microsoft Word 中单击这些形状时会显示矩形的大小，
// 第二个形状的可见外边界受到阴影和轮廓的影响，因此更大。
// 我们可以使用“AdjustWithEffects”方法来查看形状的真实大小。
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// 创建一个 RectangleF 对象，表示一个矩形，
// 我们可以将其用作形状的坐标和边界。
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// 运行此方法以获取适合所有形状效果的矩形大小。
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// 由于形状没有边框变化效果，因此其边界尺寸不受影响。
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// 验证第一个形状的最终范围（以点为单位）。
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// 形状效果稍微移动了形状的左上角。
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// 这些效果也影响了形状的可见尺寸。
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// 这些效果也影响了形状的可见边界。
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
