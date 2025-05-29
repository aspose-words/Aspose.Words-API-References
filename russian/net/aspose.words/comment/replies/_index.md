---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words для .NET
description: Откройте для себя ответы на комментарии. Получите доступ к коллекции объектов комментариев, которые являются прямыми ответами на указанный вами комментарий, повышая вовлеченность и взаимодействие пользователей.
type: docs
weight: 110
url: /ru/net/aspose.words/comment/replies/
---
## Comment.Replies property

Возвращает коллекцию[`Comment`](../) объекты, которые являются непосредственными потомками указанного комментария.

```csharp
public CommentCollection Replies { get; }
```

## Примеры

Показывает, как распечатать все комментарии к документу и ответы на них.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Если у комментария нет предка, то это комментарий «верхнего уровня», а не комментарий типа ответа.
// Вывести все комментарии верхнего уровня вместе с возможными ответами на них.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### Смотрите также

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
