---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words for .NET
description: 发现故事表，这是与您的故事直接相关的精选表格集合，可轻松增强组织性和参与度。
type: docs
weight: 50
url: /zh/net/aspose.words/story/tables/
---
## Story.Tables property

获取故事的直接子表集合。

```csharp
public TableCollection Tables { get; }
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

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
