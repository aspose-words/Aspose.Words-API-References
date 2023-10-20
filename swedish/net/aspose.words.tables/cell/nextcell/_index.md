---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words för .NET
description: Cell NextCell fast egendom. Får nästaCell nod i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Får nästa[`Cell`](../) nod.

```csharp
public Cell NextCell { get; }
```

## Anmärkningar

Metoden kan användas när du behöver ha maskinskriven åtkomst till celler i en[`Row`](../../row/) . Om a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) noden hittas i en rad istället för en cell, den korsas automatiskt för att få en cell som finns i.

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

* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
