---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: .NET için Aspose.Words
description: Belirli bir nesne türünün ilk atasını kolayca almak için Node GetAncestor yöntemini keşfedin, böylece kodlama verimliliğinizi ve doğruluğunuzu artırın.
type: docs
weight: 110
url: /tr/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

Belirtilen nesne türünün ilk atasını alır.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| ancestorType | Type | Alınacak ata nesnenin türü. |

### Geri dönüş değeri

Belirtilen türün atası veya`hükümsüz` eğer bu tipte bir ata bulunamamışsa.

## Notlar

Ata türü, şuna eşitse eşleşir:*ancestorType* veya türetilmiş*ancestorType*.

## Örnekler

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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

Belirtilenin ilk atasını alır[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| ancestorType | NodeType | Alınacak ataların düğüm türü. |

### Geri dönüş değeri

Belirtilen türün atası veya`hükümsüz` eğer bu tipte bir ata bulunamamışsa.

## Örnekler

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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
