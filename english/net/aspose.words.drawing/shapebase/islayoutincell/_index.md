---
title: IsLayoutInCell
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it in C#.
type: docs
weight: 300
url: /net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Remarks

The default value is `true`.

Has effect only for top level shapes, the property [`WrapType`](../wraptype/) of which is set to value other than [`Inline`](../../../aspose.words/inline/).

## Examples

Shows how to determine how to display a shape in a table cell.

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

// Set the "IsLayoutInCell" property to "true" to display the shape as an inline element inside the cell's paragraph.
// The coordinate origin that will determine the shape's location will be the top left corner of the shape's cell.
// If we re-size the cell, the shape will move to maintain the same position starting from the cell's top left.
// Set the "IsLayoutInCell" property to "false" to display the shape as an independent floating shape.
// The coordinate origin that will determine the shape's location will be the top left corner of the page,
// and the shape will not respond to any re-sizing of its cell.
shape.IsLayoutInCell = isLayoutInCell;

// We can only apply the "IsLayoutInCell" property to floating shapes.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
