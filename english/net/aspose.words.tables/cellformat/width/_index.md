---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: Discover the CellFormat Width property to easily measure cell width in points, enhancing your spreadsheet's layout and readability.
type: docs
weight: 140
url: /net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Gets the width of the cell in points.

```csharp
public double Width { get; set; }
```

## Remarks

The width is calculated by Aspose.Words on document loading and saving. Currently, not every combination of table, cell and document properties is supported. The returned value may not be accurate for some documents. It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended. There is no guarantee that the cell will actually have the set width. The width may be adjusted to accommodate cell contents in an auto-fit table layout. Cells in other rows may have conflicting width settings. The table may be resized to fit into the container or to meet table width settings. Consider using [`PreferredWidth`](../preferredwidth/) for setting the cell width. Setting this property sets [`PreferredWidth`](../preferredwidth/) implicitly since version 15.8.

## Examples

Shows how to format cells with a document builder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Insert a second cell, and then configure cell text padding options.
// The builder will apply these settings at its current cell, and any new cells creates afterwards.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// The first cell was unaffected by the padding reconfiguration, and still holds the default values.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// The first cell will still grow in the output document to match the size of its neighboring cell.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
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

* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
