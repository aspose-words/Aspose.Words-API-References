---
title: CellFormat.HorizontalMerge
linktitle: HorizontalMerge
articleTitle: HorizontalMerge
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CellFormat HorizontalMerge för att sömlöst sammanfoga celler horisontellt, vilket förbättrar layouten och organisationen i ditt kalkylblad.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/cellformat/horizontalmerge/
---
## CellFormat.HorizontalMerge property

Anger hur cellen sammanfogas horisontellt med andra celler i raden.

```csharp
public CellMerge HorizontalMerge { get; set; }
```

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

### Se även

* property [VerticalMerge](../verticalmerge/)
* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
