---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode HasChildNodes 财产. 返回真的如果该节点有任何子节点 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

返回`真的`如果该节点有任何子节点.

```csharp
public bool HasChildNodes { get; }
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

### 也可以看看

* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
