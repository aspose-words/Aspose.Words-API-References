---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Tables.AutoFitBehavior enum. Determines how Aspose.Words resizes the table when you invoke the AutoFit method in C#.
type: docs
weight: 6040
url: /net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Determines how Aspose.Words resizes the table when you invoke the [`AutoFit`](../table/autofit/) method.

```csharp
public enum AutoFitBehavior
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout. |
| AutoFitToWindow | `1` | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout. |
| FixedColumnWidths | `2` | Aspose.Words disables the AutoFit option and removes the preferred with from the table. |

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

Shows how to build a formatted 2x2 table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### See Also

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
