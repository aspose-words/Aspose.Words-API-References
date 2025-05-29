---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Узнайте, как составить список свойств документа и получить доступ к сведениям о владельце без усилий. Раскройте свой потенциал управления документами сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.lists/list/document/
---
## List.Document property

Получает документ владельца.

```csharp
public DocumentBase Document { get; }
```

## Примечания

Список всегда имеет родительский документ и действителен только в контексте этого документа.

## Примеры

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
* class [List](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
