---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.FlipOrientation 枚举，获取多种形状方向选项。灵活定制，提升您的文档设计！
type: docs
weight: 1290
url: /zh/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

形状方向的可能值。

```csharp
[Flags]
public enum FlipOrientation
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 坐标未翻转。 |
| Horizontal | `1` | 沿 y 轴翻转，反转 x 坐标。 |
| Vertical | `2` | 沿 x 轴翻转，反转 y 坐标。 |
| Both | `3` | 沿 y 轴和 x 轴翻转。 |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
