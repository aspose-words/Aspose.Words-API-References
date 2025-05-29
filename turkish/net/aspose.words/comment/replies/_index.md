---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: .NET için Aspose.Words
description: Yorum Yanıtlarını Keşfedin. Belirtilen yorumunuza doğrudan yanıtlar olan Yorum nesneleri koleksiyonuna erişin, kullanıcı katılımını ve etkileşimini geliştirin.
type: docs
weight: 110
url: /tr/net/aspose.words/comment/replies/
---
## Comment.Replies property

Bir koleksiyon döndürür[`Comment`](../) belirtilen yorumun doğrudan çocukları olan nesneler.

```csharp
public CommentCollection Replies { get; }
```

## Örnekler

Bir belgenin tüm yorumlarının ve bunların yanıtlarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Eğer bir yorumun bir atası yoksa, bu bir yanıt türü yorumun aksine "en üst düzey" yorumdur.
// Tüm üst düzey yorumları ve bunlara ait tüm yanıtları yazdır.
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

### Ayrıca bakınız

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
