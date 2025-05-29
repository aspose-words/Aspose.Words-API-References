---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: .NET için Aspose.Words
description: Üst Yorum nesnesini Ata özelliğimizle alın. Yorum dizilerinde gezinmek ve kullanıcı etkileşimini artırmak için mükemmeldir.
type: docs
weight: 20
url: /tr/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Üst öğeyi döndürür[`Comment`](../)nesne. Geri döner`hükümsüz` en üst düzey yorumlar için.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
