---
title: CellVerticalAlignment Enum
linktitle: CellVerticalAlignment
articleTitle: CellVerticalAlignment
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Tables.CellVerticalAlignment enum for optimal text alignment in table cells. Enhance your document layout effortlessly!
type: docs
weight: 7130
url: /net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

Specifies vertical justification of text inside a table cell.

```csharp
public enum CellVerticalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Top | `0` | Text is aligned at the top of a cell. |
| Center | `1` | Text is aligned in the middle of a cell. |
| Bottom | `2` | Text is aligned at the bottom of the cell. |

## Examples

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

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
