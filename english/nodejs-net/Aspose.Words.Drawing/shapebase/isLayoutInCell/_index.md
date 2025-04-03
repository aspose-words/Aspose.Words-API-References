---
title: ShapeBase.isLayoutInCell property
linktitle: isLayoutInCell property
articleTitle: isLayoutInCell property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.isLayoutInCell property. Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it."
type: docs
weight: 280
url: /nodejs-net/aspose.words.drawing/shapebase/isLayoutInCell/
---

## ShapeBase.isLayoutInCell property

Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.


```js
get isLayoutInCell(): boolean
```

### Remarks

The default value is ``true``.

Has effect only for top level shapes, the property [ShapeBase.wrapType](../wrapType/) of which is set to value
other than [Inline](../../../aspose.words/inline/).




### Examples

Shows how to determine how to display a shape in a table cell.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.insertCell();
builder.endTable();

let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
tableStyle.bottomPadding = 20;
tableStyle.leftPadding = 10;
tableStyle.rightPadding = 10;
tableStyle.topPadding = 20;
tableStyle.borders.color = "#000000";
tableStyle.borders.lineStyle = aw.LineStyle.Single;

table.style = tableStyle;

builder.moveTo(table.firstRow.firstCell.firstParagraph);

let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 50,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 100, 100, 100, aw.Drawing.WrapType.None);

// Set the "IsLayoutInCell" property to "true" to display the shape as an inline element inside the cell's paragraph.
// The coordinate origin that will determine the shape's location will be the top left corner of the shape's cell.
// If we re-size the cell, the shape will move to maintain the same position starting from the cell's top left.
// Set the "IsLayoutInCell" property to "false" to display the shape as an independent floating shape.
// The coordinate origin that will determine the shape's location will be the top left corner of the page,
// and the shape will not respond to any re-sizing of its cell.
shape.isLayoutInCell = isLayoutInCell;

// We can only apply the "IsLayoutInCell" property to floating shapes.
shape.wrapType = aw.Drawing.WrapType.None;

doc.save(base.artifactsDir + "Shape.LayoutInTableCell.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

