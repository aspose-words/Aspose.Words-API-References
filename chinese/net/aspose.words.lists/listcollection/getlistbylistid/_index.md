---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words for .NET
description: 使用 GetListByListId 方法轻松检索所需列表。使用简单的列表标识符快速访问数据，提高效率。
type: docs
weight: 80
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

返回列表对象。返回`无效的`如果未找到具有指定标识符的列表。

## 评论

通常情况下，你不需要使用此方法。大多数情况下，你只需设置[`List`](../../listformat/list/)property 的[`ListFormat`](../../listformat/)目的。

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

* class [List](../../list/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
