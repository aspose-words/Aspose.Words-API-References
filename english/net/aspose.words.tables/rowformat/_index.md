---
title: RowFormat Class
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.RowFormat class. Represents all formatting for a table row in C#.
type: docs
weight: 6300
url: /net/aspose.words.tables/rowformat/
---
## RowFormat class

Represents all formatting for a table row.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public class RowFormat
```

## Properties

| Name | Description |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | True if the text in a table row is allowed to split across a page break. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Gets the collection of default cell borders for the row. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Gets or sets the height of the table row in points. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Gets or sets the rule for determining the height of the table row. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Resets to default row formatting. |

## Examples

Shows how to modify formatting of a table row.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
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

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
