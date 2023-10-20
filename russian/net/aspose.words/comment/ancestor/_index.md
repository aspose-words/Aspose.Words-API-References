---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words для .NET
description: Comment Ancestor свойство. Возвращает родительский элементComment объект. Возвратнулевой для комментариев верхнего уровня на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Возвращает родительский элемент[`Comment`](../) объект. Возврат`нулевой` для комментариев верхнего уровня.

```csharp
public Comment Ancestor { get; }
```

## Примеры

Показывает, как распечатать все комментарии к документу и ответы на них.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Если комментарий не имеет предка, это комментарий «верхнего уровня», а не комментарий типа ответа.
// Распечатываем все комментарии верхнего уровня вместе со всеми ответами, которые они могут иметь.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
