---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words för .NET
description: Row NextRow fast egendom. Får nästaRow nod i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Får nästa[`Row`](../) nod.

```csharp
public Row NextRow { get; }
```

## Anmärkningar

Metoden kan användas när du behöver ha maskinskriven åtkomst till tabellrader. Om a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)noden hittas i en tabell istället för en rad, den korsas automatiskt för att få en rad som finns inom.

## Exempel

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
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
