---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: 用于 .NET 的 Aspose.Words
description: Node GetAncestor 方法. 获取指定对象类型的第一个祖先 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

获取指定对象类型的第一个祖先。

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | Type | 要检索的祖先的对象类型。 |

### 返回值

指定类型的祖先或`无效的`如果没有找到这种类型的祖先。

## 评论

如果等于，则祖先类型匹配*ancestorType*或源自*ancestorType*。

## 例子

演示如何查明表是否嵌套。

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // 查明表中的任何单元格是否有其他表作为子项。
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // 查明该表是否嵌套在另一个表内，如果是，嵌套深度是多少。
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
/// <returns>
/// 一个整数，表示表的嵌套深度（父表节点数）。
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
/// 确定表的单元格中是否包含任何直接子表。
/// 不要递归遍历这些表来检查其他表。
/// </summary>
/// <returns>
/// 如果至少一个子单元格包含表格，则返回 true。
/// 如果表中没有单元格包含表，则返回 false。
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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

获取指定的第一个祖先[`NodeType`](../../nodetype/).

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | NodeType | 要检索的祖先的节点类型。 |

### 返回值

指定类型的祖先或`无效的`如果没有找到这种类型的祖先。

## 例子

演示如何查明表是否嵌套。

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // 查明表中的任何单元格是否有其他表作为子项。
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // 查明该表是否嵌套在另一个表内，如果是，嵌套深度是多少。
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
/// <returns>
/// 一个整数，表示表的嵌套深度（父表节点数）。
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
/// 确定表的单元格中是否包含任何直接子表。
/// 不要递归遍历这些表来检查其他表。
/// </summary>
/// <returns>
/// 如果至少一个子单元格包含表格，则返回 true。
/// 如果表中没有单元格包含表，则返回 false。
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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
