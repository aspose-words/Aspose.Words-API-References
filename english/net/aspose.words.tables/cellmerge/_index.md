---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Tables.CellMerge enum for efficient table cell merging. Enhance your document layouts with seamless integration and flexibility.
type: docs
weight: 7200
url: /net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Specifies how a cell in a table is merged with other cells.

```csharp
public enum CellMerge
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The cell is not merged. |
| First | `1` | The cell is the first cell in a range of merged cells. |
| Previous | `2` | The cell is merged to the previous cell horizontally or vertically. |

## Examples

Shows how to merge table cells horizontally.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of horizontally merged cells.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insert a cell into the second column of the first row. Instead of adding text contents,
// we will merge this cell with the first cell that we added directly to the left.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Insert two more unmerged cells to the second row.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Prints the horizontal and vertical merge type of a cell.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Shows how to merge table cells vertically.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of vertically merged cells.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insert a cell into the second column of the first row, then end the row.
// Also, configure the builder to disable vertical merging in created cells.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

// Insert a cell into the first column of the second row. 
// Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Insert another independent cell in the second column of the second row.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### See Also

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
