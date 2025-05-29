---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用 RevisionGroupCollection Item 属性轻松访问特定修订组。通过精确索引增强数据管理。
type: docs
weight: 20
url: /zh/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

返回指定索引处的修订组。

```csharp
public RevisionGroup this[int index] { get; }
```

## 例子

展示如何获取文档中的一组修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### 也可以看看

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
