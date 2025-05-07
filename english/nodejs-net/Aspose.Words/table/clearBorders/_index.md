---
title: Table.clearBorders method
linktitle: clearBorders method
articleTitle: clearBorders method
second_title: Aspose.Words for Node.js
description: "Table.clearBorders method. Removes all table and cell borders on this table."
type: docs
weight: 360
url: /nodejs-net/aspose.words/table/clearBorders/
---

## clearBorders() {#default}

Removes all table and cell borders on this table.


```js
clearBorders()
```

### Examples

Shows how to apply an outline border to a table.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);

// Align the table to the center of the page.
table.alignment = aw.Tables.TableAlignment.Center;

// Clear any existing borders and shading from the table.
table.clearBorders();
table.clearShading();

// Add green borders to the outline of the table.
table.setBorder(aw.BorderType.Left, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Right, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Top, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Bottom, aw.LineStyle.Single, 1.5, "#008000", true);

// Fill the cells with a light green solid color.
table.setShading(aw.TextureIndex.TextureSolid, "#90EE90", "#000000");

doc.save(base.artifactsDir + "Table.SetOutlineBorders.docx");
```

Shows how to remove all borders from a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Hello world!");
builder.endTable();

// Modify the color and thickness of the top border.
let topBorder = table.firstRow.rowFormat.borders.at(aw.BorderType.Top);
table.setBorder(aw.BorderType.Top, aw.LineStyle.Double, 1.5, "#FF0000", true);

expect(topBorder.lineWidth).toEqual(1.5);
expect(topBorder.color).toEqual("#FF0000");
expect(topBorder.lineStyle).toEqual(aw.LineStyle.Double);

// Clear the borders of all cells in the table, and then save the document.
table.clearBorders();
expect(topBorder.color).not.toEqual("");
doc.save(base.artifactsDir + "Table.clearBorders.docx");

// Verify the values of the table's properties after re-opening the document.
doc = new aw.Document(base.artifactsDir + "Table.clearBorders.docx");
table = doc.firstSection.body.tables.at(0);
topBorder = table.firstRow.rowFormat.borders.at(aw.BorderType.Top);

expect(topBorder.lineWidth).toEqual(0.0);
expect(topBorder.color).toEqual(base.emptyColor);
expect(topBorder.lineStyle).toEqual(aw.LineStyle.None);
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

