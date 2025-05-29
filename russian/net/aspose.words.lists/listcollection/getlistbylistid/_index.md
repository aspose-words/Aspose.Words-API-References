---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words для .NET
description: Получите нужный вам список без усилий с помощью метода GetListByListId. Быстрый доступ к данным с помощью простого идентификатора списка для повышения эффективности.
type: docs
weight: 80
url: /ru/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Получает список по идентификатору списка.

```csharp
public List GetListByListId(int listId)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| listId | Int32 | Идентификатор списка. |

### Возвращаемое значение

Возвращает объект списка. Возвращает`нулевой` если список с указанным идентификатором не найден.

## Примечания

Обычно вам не нужно использовать этот метод. В большинстве случаев вы применяете форматирование списка к абзацам, просто устанавливая[`List`](../../listformat/list/) property из[`ListFormat`](../../listformat/) объект.

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

* class [List](../../list/)
* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
