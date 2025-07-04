---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words for .NET
description: Discover how the ConvertToHorizontallyMergedCells method transforms wide merged cells into horizontally merged ones, enhancing your data organization.
type: docs
weight: 410
url: /net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Converts cells horizontally merged by width to cells merged by [`HorizontalMerge`](../../cellformat/horizontalmerge/).

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Remarks

Table cells can be horizontally merged either using merge flags [`HorizontalMerge`](../../cellformat/horizontalmerge/) or using cell width [`Width`](../../cellformat/width/).

When table cell is merged by width property [`HorizontalMerge`](../../cellformat/horizontalmerge/) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.

## Examples

Shows how to convert cells horizontally merged by width to cells merged by CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word does not write merge flags anymore, defining merged cells by width instead.
// Aspose.Words by default define only 5 cells in a row, and none of them have the horizontal merge flag,
// even though there were 7 cells in the row before the horizontal merging took place.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.That(row.Cells.Count, Is.EqualTo(5));
Assert.That(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None), Is.True);

// Use the "ConvertToHorizontallyMergedCells" method to convert cells horizontally merged
// by its width to the cell horizontally merged by flags.
// Now, we have 7 cells, and some of them have horizontal merge values.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.That(row.Cells.Count, Is.EqualTo(7));

Assert.That(row.Cells[0].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.None));
Assert.That(row.Cells[1].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.First));
Assert.That(row.Cells[2].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.Previous));
Assert.That(row.Cells[3].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.None));
Assert.That(row.Cells[4].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.First));
Assert.That(row.Cells[5].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.Previous));
Assert.That(row.Cells[6].CellFormat.HorizontalMerge, Is.EqualTo(CellMerge.None));
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
