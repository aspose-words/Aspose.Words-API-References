---
title: Cell.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words för .NET
description: Upptäck celltabeller. Få enkel åtkomst till en samling tabeller direkt i din cell för effektiv organisation och förbättrad datahantering.
type: docs
weight: 120
url: /sv/net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

Hämtar en samling tabeller som är direkta underordnade tabeller till cellen.

```csharp
public TableCollection Tables { get; }
```

## Exempel

Visar hur man tar reda på om en tabell är kapslad.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Ta reda på om några celler i tabellen har andra tabeller som underordnade.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Ta reda på om tabellen är kapslad inuti en annan tabell, och i så fall på vilket djup.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Beräknar vilken nivå en tabell är kapslad inuti andra tabeller.
/// </summary>
/// <returns>
/// Ett heltal som anger tabellens kapslingsdjup (antal noder i överordnade tabeller).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// Avgör om en tabell innehåller någon direkt underordnad tabell i sina celler.
/// Gå inte rekursivt igenom dessa tabeller för att söka efter ytterligare tabeller.
/// </summary>
/// <returns>
/// Returnerar sant om minst en undercell innehåller en tabell.
/// Returnerar falskt om inga celler i tabellen innehåller en tabell.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Se även

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
