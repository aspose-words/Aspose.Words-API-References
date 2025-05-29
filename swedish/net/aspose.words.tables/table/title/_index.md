---
title: Table.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Tabelltitel, ställ enkelt in eller ändra tabellens titel för förbättrad tillgänglighet och förbättrad datarepresentation.
type: docs
weight: 320
url: /sv/net/aspose.words.tables/table/title/
---
## Table.Title property

Hämtar eller anger titeln för denna tabell. Tillhandahåller en alternativ textrepresentation av informationen i tabellen.

```csharp
public string Title { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Den här egenskapen är relevant för ISO/IEC 29500-kompatibla DOCX-dokument ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). När egenskapen sparas i format före ISO/IEC 29500 ignoreras den.

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

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
