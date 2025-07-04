---
title: CellFormat.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words for .NET
description: Discover the CellFormat LeftPadding property to easily adjust left spacing in points, enhancing your cell content's appearance and readability.
type: docs
weight: 60
url: /net/aspose.words.tables/cellformat/leftpadding/
---
## CellFormat.LeftPadding property

Returns or sets the amount of space (in points) to add to the left of the contents of cell.

```csharp
public double LeftPadding { get; set; }
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
Assert.That(table.FirstRow.Cells[0].CellFormat.Width, Is.EqualTo(0.0d));
Assert.That(table.FirstRow.Cells[0].CellFormat.LeftPadding, Is.EqualTo(5.4d));
Assert.That(table.FirstRow.Cells[0].CellFormat.RightPadding, Is.EqualTo(5.4d));
Assert.That(table.FirstRow.Cells[0].CellFormat.TopPadding, Is.EqualTo(0.0d));
Assert.That(table.FirstRow.Cells[0].CellFormat.BottomPadding, Is.EqualTo(0.0d));

Assert.That(table.FirstRow.Cells[1].CellFormat.Width, Is.EqualTo(250.0d));
Assert.That(table.FirstRow.Cells[1].CellFormat.LeftPadding, Is.EqualTo(30.0d));
Assert.That(table.FirstRow.Cells[1].CellFormat.RightPadding, Is.EqualTo(30.0d));
Assert.That(table.FirstRow.Cells[1].CellFormat.TopPadding, Is.EqualTo(30.0d));
Assert.That(table.FirstRow.Cells[1].CellFormat.BottomPadding, Is.EqualTo(30.0d));

// The first cell will still grow in the output document to match the size of its neighboring cell.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### See Also

* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
