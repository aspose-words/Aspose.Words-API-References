---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к определенным комментариям без усилий с помощью свойства CommentCollection Item. Извлеките комментарии по индексу для упрощенного управления контентом.
type: docs
weight: 10
url: /ru/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Извлекает[`Comment`](../../comment/) по данному индексу.

```csharp
public Comment this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Указатель коллекции. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и т. д.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается пустая ссылка.

## Примеры

Показывает, как удалять ответы на комментарии.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Ниже приведены два способа удаления ответов из комментария.
// 1 - Используйте метод "RemoveReply" для удаления ответов из комментария по отдельности:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Используйте метод "RemoveAllReplies", чтобы удалить все ответы из комментария одновременно:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Смотрите также

* class [Comment](../../comment/)
* class [CommentCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
