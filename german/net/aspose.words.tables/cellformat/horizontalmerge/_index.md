---
title: CellFormat.HorizontalMerge
linktitle: HorizontalMerge
articleTitle: HorizontalMerge
second_title: Aspose.Words für .NET
description: CellFormat HorizontalMerge eigendom. Gibt an wie die Zelle horizontal mit anderen Zellen in der Zeile zusammengeführt wird in C#.
type: docs
weight: 40
url: /de/net/aspose.words.tables/cellformat/horizontalmerge/
---
## CellFormat.HorizontalMerge property

Gibt an, wie die Zelle horizontal mit anderen Zellen in der Zeile zusammengeführt wird.

```csharp
public CellMerge HorizontalMerge { get; set; }
```

## Beispiele

Zeigt, wie Tabellenzellen horizontal zusammengeführt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Zelle in die erste Spalte der ersten Zeile einfügen.
// Diese Zelle ist die erste in einer Reihe horizontal verbundener Zellen.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Eine Zelle in die zweite Spalte der ersten Zeile einfügen. Anstatt Textinhalte hinzuzufügen,
// Wir werden diese Zelle mit der ersten Zelle zusammenführen, die wir direkt links hinzugefügt haben.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Fügen Sie zwei weitere nicht verbundene Zellen in die zweite Zeile ein.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Druckt den horizontalen und vertikalen Zusammenführungstyp einer Zelle.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows.OfType<Row>())
        foreach (Cell cell in row.Cells.OfType<Cell>())
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

### Siehe auch

* property [VerticalMerge](../verticalmerge/)
* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
