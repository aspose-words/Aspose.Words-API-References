---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words for .NET
description: Comment Ancestor mülk. Üst öğeyi döndürürComment nesne. İadelerhükümsüz üst düzey yorumlar için C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Üst öğeyi döndürür[`Comment`](../) nesne. İadeler`hükümsüz` üst düzey yorumlar için.

```csharp
public Comment Ancestor { get; }
```

## Örnekler

Bir belgedeki tüm yorumların ve yanıtların nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Bir yorumun atası yoksa bu, yanıt tipi yorumun aksine "üst düzey" bir yorumdur.
// Tüm üst düzey yorumları, olabilecek yanıtlarla birlikte yazdırın.
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

### Ayrıca bakınız

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
