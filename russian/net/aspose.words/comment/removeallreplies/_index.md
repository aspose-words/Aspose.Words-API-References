---
title: Comment.RemoveAllReplies
second_title: Справочник по API Aspose.Words для .NET
description: Comment метод. Удаляет все ответы на этот комментарий.
type: docs
weight: 160
url: /ru/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Удаляет все ответы на этот комментарий.

```csharp
public void RemoveAllReplies()
```

### Примечания

Все составляющие узлы ответов будут удалены из документа.

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

* class [Comment](../)
* пространство имен [Aspose.Words](../../comment/)
* сборка [Aspose.Words](../../../)


