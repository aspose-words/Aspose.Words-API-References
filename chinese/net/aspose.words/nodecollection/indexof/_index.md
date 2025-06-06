---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words for .NET
description: 探索 NodeCollection IndexOf 方法，以有效地找到集合中任何指定节点的从零开始的索引。
type: docs
weight: 70
url: /zh/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

返回指定节点的从零开始的索引。

```csharp
public int IndexOf(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 要定位的节点。 |

### 返回值

如果找到，则为集合中节点的从零开始的索引；否则为 -1。

## 评论

该方法执行线性搜索；因此，平均执行时间与[`Count`](../count/)。

## 例子

展示如何获取集合中节点的索引。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### 也可以看看

* class [Node](../../node/)
* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
