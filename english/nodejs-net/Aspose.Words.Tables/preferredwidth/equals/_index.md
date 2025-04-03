---
title: PreferredWidth.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for NodeJs
description: "PreferredWidth.equals method. Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../)."
type: docs
weight: 30
url: /nodejs-net/aspose.words.tables/preferredwidth/equals/
---

## equals(other) {#preferredwidth}

Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../).



```js
equals(other: Aspose.Words.Tables.PreferredWidth)
```

| Parameter | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../) |  |

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
* class [PreferredWidth](../)

