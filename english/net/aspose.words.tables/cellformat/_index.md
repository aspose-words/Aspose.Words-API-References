---
title: CellFormat
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5910
url: /net/aspose.words.tables/cellformat/
---
## CellFormat class

Represents all formatting for a table cell.

```csharp
public class CellFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Borders](borders) { get; } | Gets collection of borders of the cell. |
| [BottomPadding](bottompadding) { get; set; } | Returns or sets the amount of space (in points) to add below the contents of cell. |
| [FitText](fittext) { get; set; } | If true, fits text in the cell, compressing each paragraph to the width of the cell. |
| [HorizontalMerge](horizontalmerge) { get; set; } | Specifies how the cell is merged horizontally with other cells in the row. |
| [LeftPadding](leftpadding) { get; set; } | Returns or sets the amount of space (in points) to add to the left of the contents of cell. |
| [Orientation](orientation) { get; set; } | Returns or sets the orientation of text in a table cell. |
| [PreferredWidth](preferredwidth) { get; set; } | Returns or sets the preferred width of the cell. |
| [RightPadding](rightpadding) { get; set; } | Returns or sets the amount of space (in points) to add to the right of the contents of cell. |
| [Shading](shading) { get; } | Returns a Shading object that refers to the shading formatting for the cell. |
| [TopPadding](toppadding) { get; set; } | Returns or sets the amount of space (in points) to add above the contents of cell. |
| [VerticalAlignment](verticalalignment) { get; set; } | Returns or sets the vertical alignment of text in the cell. |
| [VerticalMerge](verticalmerge) { get; set; } | Specifies how the cell is merged with other cells vertically. |
| [Width](width) { get; set; } | Gets the width of the cell in points. |
| [WrapText](wraptext) { get; set; } | If true, wrap text for the cell. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](clearformatting)() | Resets to default cell formatting. Does not change the width of the cell. |
| [SetPaddings](setpaddings)(double, double, double, double) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |

### Examples

Shows how to modify formatting of a table cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Shows how to modify the format of rows and cells in a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Use the first row's "RowFormat" property to modify the formatting
// of the contents of all cells in this row.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Shows how to build a table with custom borders.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Increase row height to fit the vertical text.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### See Also

* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
