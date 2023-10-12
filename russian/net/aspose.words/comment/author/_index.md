---
title: Comment.Author
second_title: Справочник по API Aspose.Words для .NET
description: Comment свойство. Возвращает или задает имя автора комментария.
type: docs
weight: 30
url: /ru/net/aspose.words/comment/author/
---
## Comment.Author property

Возвращает или задает имя автора комментария.

```csharp
public string Author { get; set; }
```

### Примечания

Не может быть`нулевой`.

По умолчанию — пустая строка.

### Примеры

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
* пространство имен [Aspose.Words](../../comment/)
* сборка [Aspose.Words](../../../)


