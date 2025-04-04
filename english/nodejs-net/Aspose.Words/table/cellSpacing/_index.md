---
title: Table.cellSpacing property
linktitle: cellSpacing property
articleTitle: cellSpacing property
second_title: Aspose.Words for Node.js
description: "Table.cellSpacing property. Gets or sets the amount of space (in points) between the cells."
type: docs
weight: 100
url: /nodejs-net/aspose.words/table/cellSpacing/
---

## Table.cellSpacing property

Gets or sets the amount of space (in points) between the cells.


```js
get cellSpacing(): number
```

### Examples

Shows how to enable spacing between individual cells in a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Animal");
builder.insertCell();
builder.write("Class");
builder.endRow();
builder.insertCell();
builder.write("Dog");
builder.insertCell();
builder.write("Mammal");
builder.endTable();

table.cellSpacing = 3;

// Set the "AllowCellSpacing" property to "true" to enable spacing between cells
// with a magnitude equal to the value of the "CellSpacing" property, in points.
// Set the "AllowCellSpacing" property to "false" to disable cell spacing
// and ignore the value of the "CellSpacing" property.
table.allowCellSpacing = allowCellSpacing;

doc.save(base.artifactsDir + "Table.allowCellSpacing.html");

// Adjusting the "CellSpacing" property will automatically enable cell spacing.
table.cellSpacing = 5;

expect(table.allowCellSpacing).toEqual(true);
```

Shows how to create custom style settings for the table.

```js
let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);
 
    let table = builder.startTable();
    builder.insertCell();
    builder.write("Name");
    builder.insertCell();
    builder.write("مرحبًا");
    builder.endRow();
    builder.insertCell();
    builder.insertCell();
    builder.endTable();
 
    let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
    tableStyle.allowBreakAcrossPages = true;
    tableStyle.bidi = true;
    tableStyle.cellSpacing = 5;
    tableStyle.bottomPadding = 20;
    tableStyle.leftPadding = 5;
    tableStyle.rightPadding = 10;
    tableStyle.topPadding = 20;
    tableStyle.shading.backgroundPatternColor = "#FAEBD7";
    tableStyle.borders.color = "#0000FF";
    tableStyle.borders.lineStyle = aw.LineStyle.DotDash;
    tableStyle.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;

    table.style = tableStyle;

    // Setting the style properties of a table may affect the properties of the table itself.
    expect(table.bidi).toEqual(true);
    expect(table.cellSpacing).toEqual(5.0);
    expect(table.styleName).toEqual("MyTableStyle1");

    doc.save(base.artifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

