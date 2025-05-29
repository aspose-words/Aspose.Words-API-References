---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Tables.CellMerge für effizientes Zusammenführen von Tabellenzellen. Verbessern Sie Ihre Dokumentlayouts durch nahtlose Integration und Flexibilität.
type: docs
weight: 7120
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
| None | `0` | Die Zelle ist nicht zusammengeführt. |
| First | `1` | Die Zelle ist die erste Zelle in einem Bereich zusammengeführter Zellen. |
| Previous | `2` | Die Zelle wird horizontal oder vertikal mit der vorherigen Zelle zusammengeführt. |

## Beispiele

Zeigt, wie Tabellenzellen horizontal zusammengeführt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt eine Zelle in die erste Spalte der ersten Zeile ein.
// Diese Zelle ist die erste in einem Bereich horizontal verbundener Zellen.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Fügt eine Zelle in die zweite Spalte der ersten Zeile ein. Anstatt Textinhalt hinzuzufügen,
// Wir werden diese Zelle mit der ersten Zelle zusammenführen, die wir direkt links hinzugefügt haben.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

//Fügen Sie zwei weitere nicht verbundene Zellen in die zweite Zeile ein.
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

Zeigt, wie Tabellenzellen vertikal zusammengeführt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt eine Zelle in die erste Spalte der ersten Zeile ein.
// Diese Zelle ist die erste in einem Bereich vertikal verbundener Zellen.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Fügt eine Zelle in die zweite Spalte der ersten Zeile ein und beendet dann die Zeile.
// Konfigurieren Sie den Builder außerdem so, dass die vertikale Zusammenführung in erstellten Zellen deaktiviert wird.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

    // Fügt eine Zelle in die erste Spalte der zweiten Zeile ein.
// Anstatt Textinhalte hinzuzufügen, führen wir diese Zelle mit der ersten Zelle zusammen, die wir direkt darüber hinzugefügt haben.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Füge eine weitere unabhängige Zelle in die zweite Spalte der zweiten Zeile ein.
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
