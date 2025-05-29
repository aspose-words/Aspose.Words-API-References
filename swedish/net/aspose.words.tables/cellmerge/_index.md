---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.CellMerge-enum för effektiv sammanfogning av tabellceller. Förbättra dina dokumentlayouter med sömlös integration och flexibilitet.
type: docs
weight: 7120
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
| First | `1` | Cellen är den första cellen i ett område med sammanslagna celler. |
| Previous | `2` | Cellen sammanfogas med föregående cell horisontellt eller vertikalt. |

## Exempel

Visar hur man sammanfogar tabellceller horisontellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en cell i den första kolumnen på den första raden.
// Den här cellen blir den första i ett intervall av horisontellt sammanfogade celler.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Infoga en cell i den andra kolumnen på den första raden. Istället för att lägga till textinnehåll,
// vi kommer att sammanfoga den här cellen med den första cellen som vi lade till direkt till vänster.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Infoga ytterligare två osammanslagna celler på den andra raden.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Skriver ut den horisontella och vertikala sammanfogningstypen för en cell.

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

Visar hur man sammanfogar tabellceller vertikalt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en cell i den första kolumnen på den första raden.
// Den här cellen blir den första i ett intervall av vertikalt sammanfogade celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Infoga en cell i den andra kolumnen på den första raden och avsluta sedan raden.
// Konfigurera även byggaren för att inaktivera vertikal sammanslagning i skapade celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Infoga en cell i den första kolumnen på den andra raden.
// Istället för att lägga till textinnehåll kommer vi att sammanfoga den här cellen med den första cellen som vi lade till direkt ovanför.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Infoga ytterligare en oberoende cell i den andra kolumnen på den andra raden.
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
