---
title: TableCollection
second_title: Aspose.Words for .NET API 参考
description: 提供对Table./table节点集合的类型化访问
type: docs
weight: 6010
url: /zh/net/aspose.words.tables/tablecollection/
---
## TableCollection class

提供对[`Table`](../table)节点集合的类型化访问。

```csharp
public class TableCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words.tables/tablecollection/item) { get; } | 在给定索引处检索 **表** 。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add)(Node) | 将节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains)(Node) | 确定节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof)(Node) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert)(int, Node) | 将节点插入到集合中指定索引处。 |
| [Remove](../../aspose.words/nodecollection/remove)(Node) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat)(int) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words.tables/tablecollection/toarray#toarray_1)() | 将集合中的所有表复制到新的表数组中。 (2 methods) |

### 例子

显示如何删除文档中所有表的第一行和最后一行。

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

         // 找出表格中的任何单元格是否有其他表格作为孩子。
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

         // 找出该表是否嵌套在另一个表中，如果是，则嵌套在什么深度。
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
 /// 计算一个表嵌套在其他表中的级别。
/// </summary>
 /// <返回>
 /// 一个整数，表示表的嵌套深度（父表节点数）.
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
 /// 确定一个表是否在其单元格中包含任何直接子表。
 /// 不要递归遍历这些表来检查更多的表。
/// </summary>
 /// <返回>
/// 如果至少有一个子单元格包含一个表格，则返回 true。
 /// 如果表格中没有单元格包含表格，则返回 false。
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

显示如何确定表是否嵌套。

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

         // 找出表格中的任何单元格是否有其他表格作为孩子。
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

         // 找出该表是否嵌套在另一个表中，如果是，则嵌套在什么深度。
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
 /// 计算一个表嵌套在其他表中的级别。
/// </summary>
 /// <返回>
 /// 一个整数，表示表的嵌套深度（父表节点数）.
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
 /// 确定一个表是否在其单元格中包含任何直接子表。
 /// 不要递归遍历这些表来检查更多的表。
/// </summary>
 /// <返回>
/// 如果至少有一个子单元格包含一个表格，则返回 true。
 /// 如果表格中没有单元格包含表格，则返回 false。
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

### 也可以看看

* class [NodeCollection](../../aspose.words/nodecollection)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
