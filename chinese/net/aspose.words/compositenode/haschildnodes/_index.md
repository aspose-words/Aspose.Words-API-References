---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words for .NET
description: 使用 HasChildNodes 属性检测 CompositeNode 是否具有子节点。此重要功能可简化您的编码，从而实现高效的节点管理。
type: docs
weight: 30
url: /zh/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

返回`真的`如果此节点有任何子节点。

```csharp
public bool HasChildNodes { get; }
```

## 例子

展示如何将两个表中的行合并为一个。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 以下是从文档中获取表格的两种方法。
// 1 - 来自 Body 节点的“Tables”集合：
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - 使用“GetChild”方法：
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// 将当前表中的所有行附加到下一个表。
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// 删除空的表格容器。
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### 也可以看看

* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
