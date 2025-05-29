---
title: NodeCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Koleksiyonunuzdaki toplam düğüm sayısına kolayca erişmek, veri yönetimini ve verimliliği artırmak için NodeCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

Koleksiyondaki düğüm sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Bir bileşik düğümün alt düğüm koleksiyonunda nasıl dolaşılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına iki çalışma ve bir şekil alt düğüm olarak ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' öğesinin bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün yaşam süresi boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın hemen altındaki alt öğelerin koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz herhangi bir koşuyu veya şekli yazdırırız.
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

Bir tablonun iç içe geçmiş olup olmadığını nasıl bulacağınızı gösterir.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Tablodaki herhangi bir hücrenin alt tabloları olup olmadığını bulun.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Tablonun başka bir tablonun içinde yer alıp almadığını ve eğer yer alıyorsa hangi derinlikte olduğunu bulun.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Bir tablonun diğer tabloların içinde ne düzeyde yuvalandığını hesaplar.
/// </summary>
/// <returns>
/// Tablonun iç içe geçme derinliğini (üst tablo düğümlerinin sayısı) belirten bir tam sayı.
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
/// Bir tablonun hücreleri içerisinde herhangi bir alt tablonun bulunup bulunmadığını belirler.
/// Daha fazla tablo olup olmadığını kontrol etmek için bu tablolar arasında yinelemeli olarak gezinmeyin.
/// </summary>
/// <returns>
/// En az bir alt hücrenin tablo içermesi durumunda true döner.
/// Tabloda tablo içeren hiçbir hücre yoksa false döndürür.
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

### Ayrıca bakınız

* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
