---
title: CellCollection.ToArray
second_title: Aspose.Words for .NET API 参考
description: CellCollection 方法. 将集合中的所有单元格复制到新的单元格数组中
type: docs
weight: 20
url: /zh/net/aspose.words.tables/cellcollection/toarray/
---
## CellCollection.ToArray method

将集合中的所有单元格复制到新的单元格数组中。

```csharp
public Cell[] ToArray()
```

### 返回值

一组单元格。

### 例子

展示如何遍历文档中的所有表格并打印每个单元格的内容。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // 我们可以在行集合上使用“ToArray”方法将其克隆到数组中。
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // 我们可以在单元格集合上使用“ToArray”方法将其克隆到数组中。
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

* class [Cell](../../cell/)
* class [CellCollection](../)
* 命名空间 [Aspose.Words.Tables](../../cellcollection/)
* 部件 [Aspose.Words](../../../)


