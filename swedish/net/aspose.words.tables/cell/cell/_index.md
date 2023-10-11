---
title: Cell.Cell
second_title: Aspose.Words för .NET API Referens
description: Cell byggare. Initierar en ny instans avCell class.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/cell/cell/
---
## Cell constructor

Initierar en ny instans av[`Cell`](../) class.

```csharp
public Cell(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

### Anmärkningar

När[`Cell`](../) skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och[`ParentNode`](../../../aspose.words/node/parentnode/) är`null`.

Att lägga till[`Cell`](../) till dokumentanvändningenNode) ellerNode) på raden där du vill infoga cellen.

### Exempel

Visar hur man bygger en kapslad tabell utan att använda ett dokumentbyggare.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Skapa den yttre tabellen med tre rader och fyra kolumner och lägg sedan till den i dokumentet.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Skapa ytterligare en tabell med två rader och två kolumner och infoga den sedan i den första tabellens första cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Skapar en ny tabell i dokumentet med givna dimensioner och text i varje cell.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Du kan använda egenskaperna "Titel" och "Beskrivning" för att lägga till en titel respektive en beskrivning till din tabell.
    // Tabellen måste ha minst en rad innan vi kan använda dessa egenskaper.
    // Dessa egenskaper är meningsfulla för ISO / IEC 29500-kompatibla .docx-dokument (se klassen OoxmlCompliance).
    // Om vi sparar dokumentet i pre-ISO/IEC 29500-format ignorerar Microsoft Word dessa egenskaper.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Se även

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../cell/)
* hopsättning [Aspose.Words](../../../)


