---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words for .NET
description: 探索 ShapeBase FlipOrientation 属性，轻松切换形状的方向，轻松且富有创造力地增强您的设计。
type: docs
weight: 180
url: /zh/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

切换形状的方向。

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## 评论

默认值为None。

## 例子

展示如何沿轴翻转形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入图像形状并保持其方向为默认状态。
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// 将“FlipOrientation”属性设置为“FlipOrientation.Horizontal”以在 y 轴上翻转第二个形状，
// 使其成为第一个形状的水平镜像。
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// 将“FlipOrientation”属性设置为“FlipOrientation.Horizontal”以在 x 轴上翻转第三个形状，
// 使其成为第一个形状的垂直镜像。
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// 将“FlipOrientation”属性设置为“FlipOrientation.Horizontal”以在 x 轴和 y 轴上翻转第四个形状，
// 使其成为第一个形状的水平和垂直镜像。
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### 也可以看看

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
