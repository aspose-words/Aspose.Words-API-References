---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words для .NET
description: С легкостью удаляйте все ответы на свои комментарии с помощью метода RemoveAllReplies, обеспечивая бесперебойное обсуждение и улучшенный пользовательский опыт.
type: docs
weight: 170
url: /ru/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Удаляет все ответы на этот комментарий.

```csharp
public void RemoveAllReplies()
```

## Примечания

Все составляющие узлы ответов будут удалены из документа.

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

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
