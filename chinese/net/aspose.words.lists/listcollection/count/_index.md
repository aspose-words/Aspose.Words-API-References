---
title: ListCollection.Count
linktitle: Count
articleTitle: Count
second_title: 用于 .NET 的 Aspose.Words
description: ListCollection Count 财产. 获取文档中编号列表和项目符号列表的计数 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

获取文档中编号列表和项目符号列表的计数。

```csharp
public int Count { get; }
```

## 例子

演示如何验证列表的所有者文档属性。

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);
Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

### 也可以看看

* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
