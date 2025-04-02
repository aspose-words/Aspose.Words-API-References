---
title: Table.styleIdentifier property
linktitle: styleIdentifier property
articleTitle: styleIdentifier property
second_title: Aspose.Words for NodeJs
description: "Table.styleIdentifier property. Gets or sets the locale independent style identifier of the table style applied to this table."
type: docs
weight: 280
url: /nodejs-net/Aspose.Words/table/styleIdentifier/
---

## Table.styleIdentifier property

Gets or sets the locale independent style identifier of the table style applied to this table.


```js
get styleIdentifier(): Aspose.Words.StyleIdentifier
```

### Examples

Shows how to build a new table while applying a style.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let table = builder.startTable();

// We must insert at least one row before setting any table formatting.
builder.insertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table.styleIdentifier = aw.StyleIdentifier.MediumShading1Accent1;

// Partially apply the style to features of the table based on predicates, then build the table.
table.styleOptions =
  aw.Tables.TableStyleOptions.FirstColumn | aw.Tables.TableStyleOptions.RowBands | aw.Tables.TableStyleOptions.FirstRow;
table.autoFit(aw.Tables.AutoFitBehavior.AutoFitToContents);

builder.writeln("Item");
builder.cellFormat.rightPadding = 40;
builder.insertCell();
builder.writeln("Quantity (kg)");
builder.endRow();

builder.insertCell();
builder.writeln("Apples");
builder.insertCell();
builder.writeln("20");
builder.endRow();

builder.insertCell();
builder.writeln("Bananas");
builder.insertCell();
builder.writeln("40");
builder.endRow();

builder.insertCell();
builder.writeln("Carrots");
builder.insertCell();
builder.writeln("50");
builder.endRow();

doc.save(base.artifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

