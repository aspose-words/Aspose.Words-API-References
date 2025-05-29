---
title: Row
linktitle: Row
articleTitle: Row
second_title: Aspose.Words för .NET
description: Skapa enkelt dynamiska radinstanser med vår radkonstruktor. Förenkla din datahantering och förbättra din kodningseffektivitet idag!
type: docs
weight: 10
url: /sv/net/aspose.words.tables/row/row/
---
## Row constructor

Initierar en ny instans av[`Row`](../) klass.

```csharp
public Row(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

## Anmärkningar

När[`Row`](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och[`ParentNode`](../../../aspose.words/node/parentnode/) är`null`.

Att lägga till[`Row`](../) till dokumentanvändningen[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) eller[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) i tabellen där du vill infoga raden.

## Exempel

Visar hur man bygger en kapslad tabell utan att använda en dokumentbyggare.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Skapa den yttre tabellen med tre rader och fyra kolumner och lägg sedan till den i dokumentet.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Skapa en annan tabell med två rader och två kolumner och infoga den sedan i den första tabellens första cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Skapar en ny tabell i dokumentet med de angivna dimensionerna och texten i varje cell.
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

    // Du kan använda egenskaperna "Titel" och "Beskrivning" för att lägga till en titel respektive beskrivning till din tabell.
    // Tabellen måste ha minst en rad innan vi kan använda dessa egenskaper.
    // Dessa egenskaper är betydelsefulla för ISO/IEC 29500-kompatibla .docx-dokument (se OoxmlCompliance-klassen).
    // Om vi sparar dokumentet i format före ISO/IEC 29500 ignorerar Microsoft Word dessa egenskaper.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Se även

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
