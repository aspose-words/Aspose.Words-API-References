---
title: Row.Cells
second_title: Aspose.Words for .NET API 参考
description: Row 财产. 提供对Cell该行的子节点.
type: docs
weight: 20
url: /zh/net/aspose.words.tables/row/cells/
---
## Row.Cells property

提供对[`Cell`](../../cell/)该行的子节点.

```csharp
public CellCollection Cells { get; }
```

### 例子

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

* class [CellCollection](../../cellcollection/)
* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../row/)
* 部件 [Aspose.Words](../../../)


