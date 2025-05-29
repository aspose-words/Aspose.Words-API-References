---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till tabellrader med vår typed-egenskap, vilket säkerställer sömlös datahantering och förbättrad organisation för dina projekt.
type: docs
weight: 260
url: /sv/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Ger åtkomst till tabellens rader med maskinskriven kod.

```csharp
public RowCollection Rows { get; }
```

## Exempel

Visar hur man kombinerar rader från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tabeller" i en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Använda metoden "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägger till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma tabellbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

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

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
