---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 探索 ListCollection Document 属性，轻松访问所有者文档，简化数据管理。立即解锁效率！
type: docs
weight: 20
url: /zh/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

获取所有者文档。

```csharp
public DocumentBase Document { get; }
```

## 例子

显示如何验证列表的所有者文档属性。

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
