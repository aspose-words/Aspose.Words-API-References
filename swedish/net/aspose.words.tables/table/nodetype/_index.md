---
title: Table.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table NodeType som effektivt returnerar tabelldata, vilket förbättrar din datahantering och organisation för sömlös integration.
type: docs
weight: 210
url: /sv/net/aspose.words.tables/table/nodetype/
---
## Table.NodeType property

ReturerTable .

```csharp
public override NodeType NodeType { get; }
```

## Exempel

Visar hur man går igenom en sammansatt nods träd av undernoder.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Alla noder som kan innehålla undernoder, såsom själva dokumentet, är sammansatta.
    Assert.True(doc.IsComposite);

    // Anropa den rekursiva funktionen som går igenom och skriver ut alla undernoder till en sammansatt nod.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Går rekursivt igenom ett nodträd samtidigt som typen för varje nod skrivs ut
/// med ett indrag beroende på djup samt innehållet i alla inline-noder.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Rekursiv in i noden om det är en sammansatt nod. Annars, skriv ut dess innehåll om det är en inline-nod.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
