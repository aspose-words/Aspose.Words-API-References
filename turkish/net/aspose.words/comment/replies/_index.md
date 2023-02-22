---
title: Comment.Replies
second_title: Aspose.Words for .NET API Referansı
description: Comment mülk. Bir koleksiyon döndürürComment belirtilen yorumun hemen alt öğeleri olan nesneler.
type: docs
weight: 90
url: /tr/net/aspose.words/comment/replies/
---
## Comment.Replies property

Bir koleksiyon döndürür[`Comment`](../) belirtilen yorumun hemen alt öğeleri olan nesneler.

```csharp
public CommentCollection Replies { get; }
```

### Örnekler

Bir belgenin tüm yorumlarının ve yanıtlarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Bir yorumun atası yoksa, yanıt türü bir yorumun aksine "üst düzey" bir yorumdur.
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* ad alanı [Aspose.Words](../../comment/)
* toplantı [Aspose.Words](../../../)


