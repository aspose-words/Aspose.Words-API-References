---
title: PreferredWidth class
linktitle: PreferredWidth class
articleTitle: PreferredWidth class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.PreferredWidth class. Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Tables/preferredwidth/
---

## PreferredWidth class

Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




### Remarks

Preferred width can be specified as a percentage, number of points or a special "none/auto" value.

The instances of this class are immutable.




### Properties

| Name | Description |
| --- | --- |
| [type](./type/) | Gets the unit of measure used for this preferred width value. |
| [value](./value/) | Gets the preferred width value. The unit of measure is specified in the [PreferredWidth.type](./type/) property. |

### Methods

| Name | Description |
| --- | --- |
|[ equals(other)](./equals/#preferredwidth) | Determines whether the specified [PreferredWidth](./) is equal in value to the current [PreferredWidth](./). |
|[ fromPercent(percent)](./fromPercent/#number) | A creation method that returns a new instance that represents a preferred width specified as a percentage. |
|[ fromPoints(points)](./fromPoints/#number) | A creation method that returns a new instance that represents a preferred width specified using a number of points. |

### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Cell #1");
builder.insertCell();
builder.write("Cell #2");
builder.insertCell();
builder.write("Cell #3");

table.preferredWidth = aw.Tables.PreferredWidth.fromPercent(50);

doc.save(base.artifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

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

* module [Aspose.Words.Tables](../)
* property [Table.preferredWidth](../../aspose.words/table/preferredWidth/)
* property [CellFormat.preferredWidth](../cellformat/preferredWidth/)

