---
title: Row.PreviousRow
second_title: Aspose.Words för .NET API Referens
description: Row fast egendom. Hämtar föregåendeRow nod.
type: docs
weight: 100
url: /sv/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Hämtar föregående[`Row`](../) nod.

```csharp
public Row PreviousRow { get; }
```

### Anmärkningar

Metoden kan användas när du behöver ha maskinskriven åtkomst till tabellrader. Om a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)noden hittas i en tabell istället för en rad, den korsas automatiskt för att få en rad som finns inom.

### Exempel

Visar hur man räknar upp alla tabellceller.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Räkna upp genom alla celler i tabellen.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Se även

* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../row/)
* hopsättning [Aspose.Words](../../../)


