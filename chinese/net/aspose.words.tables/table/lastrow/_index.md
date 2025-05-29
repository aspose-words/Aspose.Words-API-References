---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words for .NET
description: 发现表 LastRow 属性可以轻松访问表中的最后一行节点，从而增强数据管理和效率。
type: docs
weight: 180
url: /zh/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

返回最后一个[`Row`](../../row/)表中的节点。

```csharp
public Row LastRow { get; }
```

## 例子

展示如何删除文档中所有表格的第一行和最后一行。

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

### 也可以看看

* class [Row](../../row/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
