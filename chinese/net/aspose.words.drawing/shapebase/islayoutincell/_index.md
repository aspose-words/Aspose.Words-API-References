---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words for .NET
description: 探索 ShapeBase IsLayoutInCell 属性，控制表格中的形状位置，以增强设计灵活性并改进布局管理。
type: docs
weight: 330
url: /zh/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

获取或设置一个标志，指示形状是显示在表格内部还是外部。

```csharp
public bool IsLayoutInCell { get; set; }
```

## 评论

默认值为`真的`。

仅对顶层形状有效，属性[`WrapType`](../wraptype/)其中设置为 value 而不是[`Inline`](../../../aspose.words/inline/)。

## 例子

展示如何确定如何在表格单元格中显示形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// 将“IsLayoutInCell”属性设置为“true”以将形状显示为单元格段落内的内联元素。
// 确定形状位置的坐标原点将是形状单元格的左上角。
// 如果我们重新调整单元格的大小，形状将移动以保持从单元格左上角开始的相同位置。
// 将“IsLayoutInCell”属性设置为“false”以将形状显示为独立的浮动形状。
// 确定形状位置的坐标原点是页面的左上角，
// 并且形状不会对其单元格的任何调整大小做出反应。
shape.IsLayoutInCell = isLayoutInCell;

// 我们只能将“IsLayoutInCell”属性应用于浮动形状。
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
