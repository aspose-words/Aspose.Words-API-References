---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: 用于 .NET 的 Aspose.Words
description: ListCollection GetListByListId 方法. 通过列表标识符获取列表 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

通过列表标识符获取列表。

```csharp
public List GetListByListId(int listId)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listId | Int32 | 列表标识符。 |

### 返回值

返回列表对象。退货`无效的`如果未找到具有指定标识符的列表。

## 评论

您通常不需要使用此方法。大多数时候，您只需通过设置将列表格式化 应用于段落[`List`](../../listformat/list/)的 property [`ListFormat`](../../listformat/)目的。

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

* class [List](../../list/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
