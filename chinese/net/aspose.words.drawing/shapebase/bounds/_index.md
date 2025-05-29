---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words for .NET
description: 探索 ShapeBase Bounds 属性，轻松管理形状的位置和大小，提高设计精度和效率。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

获取或设置形状包含块的位置和大小。

```csharp
public RectangleF Bounds { get; set; }
```

## 评论

设置时忽略纵横比锁定。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

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

展示如何创建和填充组形状。

```csharp
Document doc = new Document();

// 创建一个组形状。组形状可以显示子形状节点的集合。
// 在 Microsoft Word 中，单击组形状的边界或组形状的某个子形状将
// 选择此组内的所有其他子形状，并允许我们一次缩放和移动所有形状。
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// 创建一个 400pt x 400pt 的组形状并将其放置在文档的浮动形状坐标原点处。
group.Bounds = new RectangleF(0, 0, 400, 400);

 // 将组的内部坐标平面大小设置为 500 x 500pt。
// 组的左上角的 x 和 y 坐标为 (0, 0)，
// 右下角的 x 和 y 坐标为 (500, 500)。
group.CoordSize = new Size(500, 500);

 // 将组的左上角坐标设置为（-250，-250）。
// 该组的中心现在将具有 x 和 y 坐标值 (0, 0)，
// 右下角位于 (250, 250)。
group.CoordOrigin = new Point(-250, -250);

// 创建一个矩形来显示该组形状的边界并将其添加到组中。
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// 一旦形状成为组形状的一部分，我们就可以将其作为子节点访问，然后对其进行修改。
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// 创建一个小红星并将其插入到组中。
// 将形状与组的坐标原点对齐，我们已将其移动到中心。
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// 插入一个矩形，然后在与图像相同的位置插入一个稍小的矩形。
// 我们添加到组中的新形状会与旧形状重叠。浅蓝色矩形将与红色星星部分重叠，
// 然后带有图像的形状将与浅蓝色矩形重叠，并将其用作框架。
// 我们不能使用形状的“ZOrder”属性来操纵它们在组形状内的排列。
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// 在组形状中插入一个文本框。设置“Left”属性，使文本框的右边缘
// 接触组形状的右边界。设置“Top”属性，使文本框位于组形状的右边界之外
// 组形状的边界，其顶部尺寸与组形状的底部边缘对齐。
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

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
