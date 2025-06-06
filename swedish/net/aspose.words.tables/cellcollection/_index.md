---
title: CellCollection Class
linktitle: CellCollection
articleTitle: CellCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Tables.CellCollection för enkel, maskinskriven åtkomst till Cell-noder, vilket förbättrar dokumenthantering och effektivitet.
type: docs
weight: 7100
url: /sv/net/aspose.words.tables/cellcollection/
---
## CellCollection class

Ger maskinskriven åtkomst till en samling av[`Cell`](../cell/) noder.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public class CellCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words.tables/cellcollection/item/) { get; } | Hämtar en[`Cell`](../cell/) vid det givna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Avgör om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel iteration i "foreach"-stil över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words.tables/cellcollection/toarray/#toarray_1)() | Kopierar alla celler från samlingen till en ny cellmatris. (2 methods) |

## Exempel

Visar hur man itererar igenom alla tabeller i dokumentet och skriver ut innehållet i varje cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Vi kan använda metoden "ToArray" på en radsamling för att klona den till en array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Vi kan använda metoden "ToArray" på en cellsamling för att klona den till en array.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### Se även

* class [NodeCollection](../../aspose.words/nodecollection/)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
