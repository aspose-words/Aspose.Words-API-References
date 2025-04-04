---
title: PreferredWidth.fromPercent method
linktitle: fromPercent method
articleTitle: fromPercent method
second_title: Aspose.Words for Node.js
description: "PreferredWidth.fromPercent method. A creation method that returns a new instance that represents a preferred width specified as a percentage."
type: docs
weight: 40
url: /nodejs-net/aspose.words.tables/preferredwidth/fromPercent/
---

## fromPercent(percent) {#number}

A creation method that returns a new instance that represents a preferred width specified as a percentage.


```js
fromPercent(percent: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| percent | number | The value must be from 0 to 100. |

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

* module [Aspose.Words.Tables](../../)
* class [PreferredWidth](../)

