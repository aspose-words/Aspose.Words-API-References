---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: 用于 .NET 的 Aspose.Words
description: Table Rows 财产. 提供对表行的类型化访问 在 C#.
type: docs
weight: 260
url: /zh/net/aspose.words.tables/table/rows/
---
## Table.Rows property

提供对表行的类型化访问。

```csharp
public RowCollection Rows { get; }
```

## 例子

演示如何将两个表中的行合并为一个表。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 下面是从文档中获取表格的两种方法。
// 1 - 来自 Body 节点的“Tables”集合：
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - 使用“GetChild”方法：
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// 将当前表中的所有行追加到下一个表中。
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// 删除空表容器。
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

演示如何迭代文档中的所有表格并打印每个单元格的内容。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // 我们可以对行集合使用“ToArray”方法将其克隆到数组中。
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // 我们可以对单元集合使用“ToArray”方法将其克隆到数组中。
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### 也可以看看

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
