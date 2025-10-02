---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.TextOrientation enum to easily control text alignment in table cells and text frames, enhancing document presentation and readability.
type: docs
weight: 7340
url: /net/aspose.words/textorientation/
---
## TextOrientation enumeration

Specifies orientation of text on a page, in a table cell or a text frame.

```csharp
public enum TextOrientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | `0` | Text is arranged horizontally (lr-tb). |
| Downward | `1` | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | `3` | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| HorizontalRotatedFarEast | `4` | Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v). |
| VerticalFarEast | `5` | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v). |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
