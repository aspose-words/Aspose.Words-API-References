---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words för .NET
description: Upptäck NextCell-egenskapen för att enkelt komma åt nästa Cell-nod, vilket förbättrar din datahantering och effektiviserar ditt arbetsflöde.
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

Metoden kan användas när du behöver ha skrivåtkomst till celler i en[`Row`](../../row/) Om a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Om en nod hittas i en rad istället för i en cell, genomsöks den automatiskt för att hitta en cell som finns inuti.

## Exempel

Visar hur man räknar igenom alla tabellceller.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Räkna igenom alla celler i tabellen.
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
