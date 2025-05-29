---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words для .NET
description: Легко управляйте авторами комментариев с помощью свойства Comment Author. Легко возвращайте или устанавливайте имена авторов для повышения вовлеченности пользователей и ясности контента.
type: docs
weight: 30
url: /ru/net/aspose.words/comment/author/
---
## Comment.Author property

Возвращает или задает имя автора комментария.

```csharp
public string Author { get; set; }
```

## Примечания

Не может быть`нулевой`.

По умолчанию — пустая строка.

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

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
