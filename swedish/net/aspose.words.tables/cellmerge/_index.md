---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words för .NET
description: Aspose.Words.Tables.CellMerge uppräkning. Anger hur en cell i en tabell slås samman med andra celler i C#.
type: docs
weight: 6270
url: /sv/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Anger hur en cell i en tabell slås samman med andra celler.

```csharp
public enum CellMerge
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Cellen är inte sammanfogad. |
| First | `1` | Cellen är den första cellen i ett intervall av sammanslagna celler. |
| Previous | `2` | Cellen slås samman med föregående cell horisontellt eller vertikalt. |

## Exempel

Visar hur man slår samman tabellceller horisontellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en cell i den första kolumnen på den första raden.
// Den här cellen kommer att vara den första i en rad horisontellt sammanslagna celler.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Infoga en cell i den andra kolumnen på den första raden. Istället för att lägga till textinnehåll,
// vi kommer att slå samman denna cell med den första cellen som vi la till direkt till vänster.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Infoga ytterligare två osammanfogade celler i den andra raden.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Skriver ut den horisontella och vertikala sammanslagningstypen för en cell.

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

Visar hur man slår samman tabellceller vertikalt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en cell i den första kolumnen på den första raden.
// Den här cellen kommer att vara den första i en rad vertikalt sammanslagna celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Infoga en cell i den andra kolumnen på den första raden, avsluta sedan raden.
// Konfigurera också byggaren för att inaktivera vertikal sammanslagning i skapade celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Infoga en cell i den första kolumnen på den andra raden.
// Istället för att lägga till textinnehåll kommer vi att slå samman denna cell med den första cellen som vi lade till direkt ovanför.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Infoga en annan oberoende cell i den andra kolumnen på den andra raden.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Se även

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
