---
title: CellFormat.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: Discover how to use the CellFormat Orientation property to adjust text direction in table cells, enhancing readability and design in your documents.
type: docs
weight: 70
url: /net/aspose.words.tables/cellformat/orientation/
---
## CellFormat.Orientation property

Returns or sets the orientation of text in a table cell.

```csharp
public TextOrientation Orientation { get; set; }
```

## Examples

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
Assert.That(table.Rows[0].Cells[0].CellFormat.VerticalAlignment, Is.EqualTo(CellVerticalAlignment.Center));
Assert.That(table.Rows[0].Cells[1].CellFormat.VerticalAlignment, Is.EqualTo(CellVerticalAlignment.Center));

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
Assert.That(table.Rows[0].RowFormat.Height, Is.EqualTo(0));
Assert.That(table.Rows[0].RowFormat.HeightRule, Is.EqualTo(HeightRule.Auto));
Assert.That(table.Rows[1].RowFormat.Height, Is.EqualTo(100));
Assert.That(table.Rows[1].RowFormat.HeightRule, Is.EqualTo(HeightRule.Exactly));
Assert.That(table.Rows[1].Cells[0].CellFormat.Orientation, Is.EqualTo(TextOrientation.Upward));
Assert.That(table.Rows[1].Cells[1].CellFormat.Orientation, Is.EqualTo(TextOrientation.Downward));

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### See Also

* enum [TextOrientation](../../../aspose.words/textorientation/)
* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
