---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 探索 RevisionGroupCollection 的 Count 属性。轻松检索修订组的总数，提升数据管理效率。
type: docs
weight: 10
url: /zh/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

返回集合中的修订组数。

```csharp
public int Count { get; }
```

## 例子

展示如何打印有关文档中一组修订的信息。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### 也可以看看

* class [RevisionGroupCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
