---
title: TableStyleOptions enumeration
linktitle: TableStyleOptions enumeration
articleTitle: TableStyleOptions enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.TableStyleOptions enumeration. Specifies how table style is applied to a table."
type: docs
weight: 140
url: /nodejs-net/Aspose.Words.Tables/tablestyleoptions/
---

## TableStyleOptions enumeration

Specifies how table style is applied to a table.


### Members

| Name | Description |
| --- | --- |
| None | No table style formatting is applied. |
| FirstRow | Apply first row conditional formatting. |
| LastRow | Apply last row conditional formatting. |
| FirstColumn | Apply 1 first column conditional formatting. |
| LastColumn | Apply last column conditional formatting. |
| RowBands | Apply row banding conditional formatting. |
| ColumnBands | Apply column banding conditional formatting. |
| Default2003 | Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF. |
| Default | This is Microsoft Word defaults. |

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

* module [Aspose.Words.Tables](../)
* property [Table.styleOptions](../../Aspose.Words/table/styleOptions/)

