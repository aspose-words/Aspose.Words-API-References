---
title: ListCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: ListCollection Count свойство. Получает количество нумерованных и маркированных списков в документе на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

Получает количество нумерованных и маркированных списков в документе.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как проверить свойства документов владельцев списков.

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

### Смотрите также

* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
