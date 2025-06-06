---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words for .NET
description: 探索 ShapeBase BoundsInPoints 属性，轻松访问形状的大小和位置（以点为单位），增强设计精度和布局控制。
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

获取形状包含块的位置和大小（以点为单位），相对于最顶层形状的锚点。

```csharp
public RectangleF BoundsInPoints { get; }
```

## 评论

返回的边界不包括此形状的旋转或父组形状的旋转（如果有）。

## 例子

展示如何验证包含块边界的形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// 尽管该行本身在文档页面上占用的空间很小，
// 它占据一个矩形包含块，我们可以使用“Bounds”属性确定其大小。
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// 创建一个组形状，然后使用“Bounds”属性设置其包含块的大小。
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// 创建一个矩形，验证其边界块的大小，然后将其添加到组形状中。
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// 组形状的坐标平面的原点位于其包含块的左上角，
// 右下角的 x 和 y 坐标为 (1000, 1000)。
// 我们的组形状大小为 250x250pt，因此组形状坐标平面上的每 4pt
// 在文档主体的坐标平面中转换为 1pt。
// 我们插入的每个形状的尺寸也会缩小 4 倍。
// 形状的“BoundsInPoints”属性的变化将反映这一点。
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// 插入一个形状并将其放置在组形状包含块的边界之外。
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// 组形状在文档主体中的占用空间增加了，但包含块保持不变。
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
