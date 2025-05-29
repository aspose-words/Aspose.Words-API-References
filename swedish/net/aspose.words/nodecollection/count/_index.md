---
title: NodeCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen NodeCollection Count för att enkelt komma åt det totala antalet noder i din samling, vilket förbättrar datahantering och effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

Hämtar antalet noder i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur man navigerar genom en sammansatt nods samling av underordnade noder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast finns under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av omedelbara underordnade,
// och skriv ut alla körningar eller former som vi hittar inuti.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
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

* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
