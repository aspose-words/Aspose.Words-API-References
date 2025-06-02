---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Tables.TableStyleOptions enum for flexible table styling. Enhance your document design with customizable table styles today!
type: docs
weight: 7230
url: /net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Specifies how table style is applied to a table.

```csharp
[Flags]
public enum TableStyleOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No table style formatting is applied. |
| FirstRow | `20` | Apply first row conditional formatting. |
| LastRow | `40` | Apply last row conditional formatting. |
| FirstColumn | `80` | Apply 1 first column conditional formatting. |
| LastColumn | `100` | Apply last column conditional formatting. |
| RowBands | `200` | Apply row banding conditional formatting. |
| ColumnBands | `400` | Apply column banding conditional formatting. |
| Default2003 | `600` | Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF. |
| Default | `2A0` | This is Microsoft Word defaults. |

## Examples

Shows how to build a new table while applying a style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// We must insert at least one row before setting any table formatting.
builder.InsertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Partially apply the style to features of the table based on predicates, then build the table.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### See Also

* property [StyleOptions](../table/styleoptions/)
* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
