---
title: CellCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till specifika celler med egenskapen CellCollection Item. Hämta valfri cell via index för effektiv datahantering och förbättrad prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/cellcollection/item/
---
## CellCollection indexer

Hämtar en[`Cell`](../../cell/) vid det givna indexet.

```csharp
public Cell this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

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

* class [Cell](../../cell/)
* class [CellCollection](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
