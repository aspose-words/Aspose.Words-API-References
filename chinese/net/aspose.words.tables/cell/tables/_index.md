---
title: Cell.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words for .NET
description: 探索单元格表。轻松直接访问单元格内的表格集合，从而简化组织并增强数据管理。
type: docs
weight: 120
url: /zh/net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

获取单元格的直接子表的集合。

```csharp
public TableCollection Tables { get; }
```

## 例子

显示如何确定表是否嵌套。

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // 查明表格中是否有单元格具有其他表格作为子表格。
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // 查明表是否嵌套在另一个表中，如果是，则嵌套深度是多少。
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
/// 一个整数，表示表的嵌套深度（父表节点的数量）。
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
/// 确定表的单元格内是否包含任何直接子表。
/// 不要递归遍历这些表来检查进一步的表。
/// </summary>
/// <returns>
/// 如果至少有一个子单元格包含表格，则返回 true。
/// 如果表格中没有单元格包含表格，则返回 false。
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

### 也可以看看

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
