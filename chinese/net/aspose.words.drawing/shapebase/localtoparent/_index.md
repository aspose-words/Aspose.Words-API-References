---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase LocalToParent 方法. 将局部坐标空间中的值转换为父形状的坐标空间 在 C#.
type: docs
weight: 670
url: /zh/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

将局部坐标空间中的值转换为父形状的坐标空间。

```csharp
public PointF LocalToParent(PointF value)
```

## 例子

演示如何将形状坐标平面上的 x 和 y 坐标位置转换为父形状坐标平面上的位置。

```csharp
Document doc = new Document();

// 插入一个组形状，并将其放置在 100 点下方和右侧
// 文档的 x 和 Y 坐标原点。
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// 使用“LocalToParent”方法确定组内部 x 和 y 坐标上的 (0, 0)
// 位于其父形状坐标系的 (100, 100) 上。组形状的父级是文档本身。
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// 默认情况下，形状的内部坐标平面的左上角位于 (0, 0)，
// 以及右下角 (1000, 1000)。由于其尺寸，我们的组形状覆盖 500pt x 500pt 的面积
// 在文档的平面上。这意味着文档坐标平面上 1pt 的移动将会平移
// 在组形状的坐标平面上移动 2 点。
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// 将组形状的 x 轴和 y 轴原点从左上角移动到中心。
// 这将使组的内部坐标相对于文档的坐标进一步偏移。
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// 改变坐标平面的比例也会影响相对位置。
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// 如果我们希望向该组添加形状，同时根据文档中的位置定义其位置，
// 我们需要首先确认组形状中与文档位置相匹配的位置。
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
