---
title: Row.Cells
linktitle: Cells
articleTitle: Cells
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till radceller med maskinskrivna kontroller för sömlös hantering av underordnade noder, vilket förbättrar din datahanteringsupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.tables/row/cells/
---
## Row.Cells property

Ger maskinskriven åtkomst till[`Cell`](../../cell/) underordnade noder till raden.

```csharp
public CellCollection Cells { get; }
```

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

* class [CellCollection](../../cellcollection/)
* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
