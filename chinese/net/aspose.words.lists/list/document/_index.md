---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 了解如何轻松列出文档属性并访问所有权详情。立即释放您的文档管理潜能！
type: docs
weight: 10
url: /zh/net/aspose.words.lists/list/document/
---
## List.Document property

获取所有者文档。

```csharp
public DocumentBase Document { get; }
```

## 评论

列表始终具有父文档，并且仅在该文档的上下文中有效。

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
* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
