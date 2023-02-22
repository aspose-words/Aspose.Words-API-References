---
title: Enum CellMerge
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Tables.CellMerge opsomming. Gibt an wie eine Zelle in einer Tabelle mit anderen Zellen zusammengeführt wird.
type: docs
weight: 5970
url: /de/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Gibt an, wie eine Zelle in einer Tabelle mit anderen Zellen zusammengeführt wird.

```csharp
public enum CellMerge
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Die Zelle wird nicht verbunden. |
| First | `1` | Die Zelle ist die erste Zelle in einem Bereich verbundener Zellen. |
| Previous | `2` | Die Zelle wird horizontal oder vertikal mit der vorherigen Zelle verbunden. |

### Beispiele

Zeigt, wie Tabellenzellen horizontal verbunden werden.

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

// Zwei weitere nicht verbundene Zellen in die zweite Zeile einfügen.
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

Zeigt, wie Tabellenzellen vertikal verbunden werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Zelle in die erste Spalte der ersten Zeile einfügen.
// Diese Zelle ist die erste in einer Reihe vertikal verbundener Zellen.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Füge eine Zelle in die zweite Spalte der ersten Zeile ein und beende dann die Zeile.
// Konfigurieren Sie außerdem den Builder, um das vertikale Zusammenführen in erstellten Zellen zu deaktivieren.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

// Eine Zelle in die erste Spalte der zweiten Zeile einfügen. 
// Anstatt Textinhalte hinzuzufügen, werden wir diese Zelle mit der ersten Zelle zusammenführen, die wir direkt darüber hinzugefügt haben.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Eine weitere unabhängige Zelle in die zweite Spalte der zweiten Zeile einfügen.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)


