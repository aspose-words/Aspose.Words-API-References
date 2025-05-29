---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: Aspose.Words för .NET
description: Upptäck Node GetAncestor-metoden för att enkelt hämta den första förfadern till en specifik objekttyp, vilket förbättrar din kodningseffektivitet och noggrannhet.
type: docs
weight: 110
url: /sv/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

Hämtar den första förfadern till den angivna objekttypen.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ancestorType | Type | Objekttypen för den förfader som ska hämtas. |

### Returvärde

Förfadern till den angivna typen eller`null` om ingen förfader av denna typ hittades.

## Anmärkningar

Förfadertypen matchar om den är lika med*ancestorType* eller härlett från*ancestorType*.

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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

Hämtar den första förfadern till den angivna[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ancestorType | NodeType | Nodtypen för den förfader som ska hämtas. |

### Returvärde

Förfadern till den angivna typen eller`null` om ingen förfader av denna typ hittades.

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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
