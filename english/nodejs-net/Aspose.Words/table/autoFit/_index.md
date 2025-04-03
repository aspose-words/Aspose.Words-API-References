---
title: Table.autoFit method
linktitle: autoFit method
articleTitle: autoFit method
second_title: Aspose.Words for NodeJs
description: "Table.autoFit method. Resizes the table and cells according to the specified auto fit behavior."
type: docs
weight: 380
url: /nodejs-net/Aspose.Words/table/autoFit/
---

## autoFit(behavior) {#autofitbehavior}

Resizes the table and cells according to the specified auto fit behavior.


```js
autoFit(behavior: Aspose.Words.Tables.AutoFitBehavior)
```

| Parameter | Type | Description |
| --- | --- | --- |
| behavior | [AutoFitBehavior](../../../aspose.words.tables/autofitbehavior/) | Specifies how to auto fit the table. |

### Remarks

This method mimics the commands available in the Auto Fit menu for a table in Microsoft Word.
The commands available are "Auto Fit to Contents", "Auto Fit to Window" and "Fixed Column Width". In Microsoft Word
these commands set relevant table properties and then update the table layout and Aspose.Words does the same for you.




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

