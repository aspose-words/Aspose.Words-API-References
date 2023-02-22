---
title: Table.NodeType
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. İade DüğümTürü.Tablo .
type: docs
weight: 210
url: /tr/net/aspose.words.tables/table/nodetype/
---
## Table.NodeType property

İade **DüğümTürü.Tablo** .

```csharp
public override NodeType NodeType { get; }
```

### Örnekler

Bir bileşik düğümün alt düğümler ağacında nasıl geçileceğini gösterir.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Belgenin kendisi gibi alt düğümler içerebilen herhangi bir düğüm bileşiktir.
    Assert.True(doc.IsComposite);

    // Bir bileşik düğümün tüm alt düğümlerini geçecek ve yazdıracak özyinelemeli işlevi çağırın.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Her bir düğümün türünü yazdırırken bir düğüm ağacında yinelemeli olarak geçer
/// tüm satır içi düğümlerin içeriğinin yanı sıra derinliğe bağlı bir girinti ile.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Bileşik bir düğümse, düğüme tekrar gir. Aksi takdirde, bir satır içi düğüm ise içeriğini yazdırın.
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

Bir tablonun iç içe olup olmadığını nasıl öğreneceğinizi gösterir.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Tablodaki herhangi bir hücrenin alt öğe olarak başka tabloları olup olmadığını öğrenin.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Tablonun başka bir tablonun içinde olup olmadığını ve öyleyse hangi derinlikte olduğunu öğrenin.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Bir tablonun diğer tabloların içinde hangi düzeyde iç içe olduğunu hesaplar.
/// </summary>
/// <returns>
/// Tablonun iç içe geçme derinliğini gösteren bir tam sayı (üst tablo düğümlerinin sayısı).
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
/// Bir tablonun hücreleri içinde herhangi bir doğrudan alt tablo içerip içermediğini belirler.
/// Daha fazla tablo olup olmadığını kontrol etmek için bu tablolar arasında tekrar tekrar dolaşmayın.
/// </summary>
/// <returns>
/// En az bir alt hücre bir tablo içeriyorsa true değerini döndürür.
/// Tablodaki hiçbir hücre tablo içermiyorsa false döndürür.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Ayrıca bakınız

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


