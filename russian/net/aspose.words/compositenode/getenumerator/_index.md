---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Изучите метод CompositeNode GetEnumerator для бесшовной итерации по дочерним узлам. Повысьте эффективность кодирования с помощью этой мощной функции!
type: docs
weight: 120
url: /ru/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла.

```csharp
public IEnumerator<Node> GetEnumerator()
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

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
