---
title: CommentCollection.Item
second_title: Справочник по API Aspose.Words для .NET
description: CommentCollection свойство. ПолучаетComment по данному индексу.
type: docs
weight: 10
url: /ru/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Получает[`Comment`](../../comment/) по данному индексу.

```csharp
public Comment this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в коллекции. |

### Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний элемент и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицателен и его абсолютное значение превышает количество элементов в списке, возвращается нулевая ссылка.

### Примеры

Показывает, как удалить ответы на комментарии.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Ниже приведены два способа удаления ответов на комментарий.
// 1 - Используйте метод "RemoveReply", чтобы удалить ответы на комментарий по отдельности:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - Используйте метод "RemoveAllReplies", чтобы удалить сразу все ответы из комментария:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Смотрите также

* class [Comment](../../comment/)
* class [CommentCollection](../)
* пространство имен [Aspose.Words](../../commentcollection/)
* сборка [Aspose.Words](../../../)


