---
title: Table.setBorders method
linktitle: setBorders method
articleTitle: setBorders method
second_title: Aspose.Words for NodeJs
description: "Table.setBorders method. Sets all table borders to the specified line style, width and color."
type: docs
weight: 440
url: /nodejs-net/Aspose.Words/table/setBorders/
---

## setBorders(lineStyle, lineWidth, color) {#linestyle_number_string}

Sets all table borders to the specified line style, width and color.


```js
setBorders(lineStyle: Aspose.Words.LineStylelineWidth: numbercolor: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | [LineStyle](../../linestyle/) | The line style to apply. |
| lineWidth | number | The line width to set (in points). |
| color | string | The color to use for the border. |

### Examples

Shows how to apply border and shading color while building a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Start a table and set a default color/thickness for its borders.
let table = builder.startTable();
table.setBorders(aw.LineStyle.Single, 2.0, "#000000");

// Create a row with two cells with different background colors.
builder.insertCell();
builder.cellFormat.shading.backgroundPatternColor = "#87CEFA";
builder.writeln("Row 1, Cell 1.");
builder.insertCell();
builder.cellFormat.shading.backgroundPatternColor = "#FFA500";
builder.writeln("Row 1, Cell 2.");
builder.endRow();

// Reset cell formatting to disable the background colors
// set a custom border thickness for all new cells created by the builder,
// then build a second row.
builder.cellFormat.clearFormatting();
builder.cellFormat.borders.left.lineWidth = 4.0;
builder.cellFormat.borders.right.lineWidth = 4.0;
builder.cellFormat.borders.top.lineWidth = 4.0;
builder.cellFormat.borders.bottom.lineWidth = 4.0;

builder.insertCell();
builder.writeln("Row 2, Cell 1.");
builder.insertCell();
builder.writeln("Row 2, Cell 2.");

doc.save(base.artifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

Shows how to format of all of a table's borders at once.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);

// Clear all existing borders from the table.
table.clearBorders();

// Set a single green line to serve as every outer and inner border of this table.
table.setBorders(aw.LineStyle.Single, 1.5, "#008000");

doc.save(base.artifactsDir + "Table.setBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

