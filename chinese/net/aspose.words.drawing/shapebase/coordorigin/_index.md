---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase CoordOrigin 财产. 该形状的包含块左上角的坐标 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

该形状的包含块左上角的坐标。

```csharp
public Point CoordOrigin { get; set; }
```

## 评论

默认值为 (0,0)。

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

展示如何创建和填充组形状。

```csharp
Document doc = new Document();

// 创建一个组形状。组形状可以显示子形状节点的集合。
// 在 Microsoft Word 中，单击组形状的边界内或组形状的子形状之一将
// 选择该组中的所有其他子形状，并允许我们一次缩放和移动所有形状。
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// 创建一个 400pt x 400pt 的组形状并将其放置在文档的浮动形状坐标原点处。
group.Bounds = new RectangleF(0, 0, 400, 400);

// 将组的内部坐标平面大小设置为 500 x 500pt。 
// 该组的左上角的 x 和 y 坐标为 (0, 0)，
// 右下角的 x 和 y 坐标为 (500, 500)。
group.CoordSize = new Size(500, 500);

// 设置组左上角的坐标为(-250,-250)。 
// 该组的中心现在的 x 和 y 坐标值为 (0, 0)，
// 右下角将位于 (250, 250)。
group.CoordOrigin = new Point(-250, -250);

// 创建一个矩形来显示该组形状的边界并将其添加到组中。
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// 一旦形状成为组形状的一部分，我们就可以将其作为子节点访问，然后对其进行修改。
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// 创建一个小红星并将其插入到组中。
// 将形状与组的坐标原点对齐，我们已将其移动到中心。
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// 插入一个矩形，然后在与图像相同的位置插入一个稍小的矩形。 
// 我们添加到组中的新形状与旧形状重叠。浅蓝色矩形将部分重叠红色星星，
// 然后带有图像的形状将与浅蓝色矩形重叠，将其用作框架。
// 我们不能使用形状的“ZOrder”属性来操纵它们在组形状内的排列。 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// 将文本框插入组形状中。设置“Left”属性，使文本框的右边缘
// 触及组形状的右边界。设置“Top”属性，使文本框位于外部
// 组形状的边界，其顶部尺寸沿着组形状的底部边距对齐。
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
