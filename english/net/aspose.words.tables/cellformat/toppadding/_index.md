---
title: CellFormat.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words for .NET
description: CellFormat TopPadding property. Returns or sets the amount of space in points to add above the contents of cell in C#.
type: docs
weight: 100
url: /net/aspose.words.tables/cellformat/toppadding/
---
## CellFormat.TopPadding property

Returns or sets the amount of space (in points) to add above the contents of cell.

```csharp
public double TopPadding { get; set; }
```

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

### See Also

* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
