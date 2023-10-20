---
title: Table
linktitle: Table
articleTitle: Table
second_title: Aspose.Words för .NET
description: Table byggare. Initierar en ny instans avTable class i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/table/table/
---
## Table constructor

Initierar en ny instans av[`Table`](../) class.

```csharp
public Table(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

## Anmärkningar

När[`Table`](../) skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och[`ParentNode`](../../../aspose.words/node/parentnode/) är`null`.

Att lägga till[`Table`](../) till dokumentanvändningen[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) eller[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) på berättelsen där du vill att tabellen ska infogas.

## Exempel

Visar hur man skapar en tabell.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabeller innehåller rader, som innehåller celler, som kan ha stycken
// med typiska element som körningar, former och till och med andra tabeller.
// Att anropa metoden "EnsureMinimum" på en tabell säkerställer det
// tabellen har minst en rad, cell och stycke.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Lägg till text till det första anropet i den första raden i tabellen.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

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
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
