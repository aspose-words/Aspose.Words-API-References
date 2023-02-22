---
title: ListCollection.Document
second_title: Справочник по API Aspose.Words для .NET
description: ListCollection свойство. Получает документ владельца.
type: docs
weight: 20
url: /ru/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Получает документ владельца.

```csharp
public DocumentBase Document { get; }
```

### Примеры

Показывает, как проверить свойства документа владельца списков.

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../listcollection/)
* сборка [Aspose.Words](../../../)


