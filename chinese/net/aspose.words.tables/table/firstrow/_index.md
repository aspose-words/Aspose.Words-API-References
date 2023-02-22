---
title: Table.FirstRow
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 返回第一个 排表中的节点
type: docs
weight: 160
url: /zh/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

返回第一个 **排**表中的节点。

```csharp
public Row FirstRow { get; }
```

### 例子

演示如何删除文档中所有表格的第一行和最后一行。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

显示如何将两个表中的行合并为一个。

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

### 也可以看看

* class [Row](../../row/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


