---
title: PreferredWidth.fromPoints method
linktitle: fromPoints method
articleTitle: fromPoints method
second_title: Aspose.Words for NodeJs
description: "PreferredWidth.fromPoints method. A creation method that returns a new instance that represents a preferred width specified using a number of points."
type: docs
weight: 50
url: /nodejs-net/aspose.words.tables/preferredwidth/fromPoints/
---

## fromPoints(points) {#number}

A creation method that returns a new instance that represents a preferred width specified using a number of points.


```js
fromPoints(points: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | number | The value must be from 0 to 22 inches (22 \* 72 points). |

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

Shows how to use unit conversion tools while specifying a preferred width for a cell.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.fromPoints(aw.ConvertUtil.inchToPoint(3));
builder.insertCell();

expect(table.firstRow.firstCell.cellFormat.preferredWidth.value).toEqual(216.0);
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [PreferredWidth](../)

