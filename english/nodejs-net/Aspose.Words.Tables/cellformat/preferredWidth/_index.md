---
title: CellFormat.preferredWidth property
linktitle: preferredWidth property
articleTitle: preferredWidth property
second_title: Aspose.Words for NodeJs
description: "CellFormat.preferredWidth property. Returns or sets the preferred width of the cell."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Tables/cellformat/preferredWidth/
---

## CellFormat.preferredWidth property

Returns or sets the preferred width of the cell.


```js
get preferredWidth(): Aspose.Words.Tables.PreferredWidth
```

### Remarks

The preferred width (along with the table's Auto Fit option) determines how the actual
width of the cell is calculated by the table layout algorithm. Table layout can be performed by
Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width
can also be specified as "auto", which means no preferred width is specified.

The default value is Aspose.Words.Tables.PreferredWidth.Auto.




### Examples

Shows how to set a preferred width for table cells.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let table = builder.startTable();

// There are two ways of applying the "PreferredWidth" class to table cells.
// 1 -  Set an absolute preferred width based on points:
builder.insertCell();
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.fromPoints(40);
builder.cellFormat.shading.backgroundPatternColor = "#FFFFE0";
builder.writeln(`Cell with a width of ${builder.cellFormat.preferredWidth}.`);

// 2 -  Set a relative preferred width based on percent of the table's width:
builder.insertCell();
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.fromPercent(20);
builder.cellFormat.shading.backgroundPatternColor = "#ADD8E6";
builder.writeln(`Cell with a width of ${builder.cellFormat.preferredWidth}.`);

builder.insertCell();

// A cell with no preferred width specified will take up the rest of the available space.
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.auto;

builder.cellFormat.shading.backgroundPatternColor = "#90EE90";
builder.writeln("Automatically sized cell.");

doc.save(base.artifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)
* property [CellFormat.width](../width/)

