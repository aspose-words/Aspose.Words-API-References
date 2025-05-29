---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: .NET için Aspose.Words
description: Yorum Yazarı özelliğiyle yorum yazarlarını zahmetsizce yönetin. Kullanıcı etkileşimini ve içerik netliğini artırmak için yazar adlarını kolayca döndürün veya ayarlayın.
type: docs
weight: 30
url: /tr/net/aspose.words/comment/author/
---
## Comment.Author property

Bir yorumun yazar adını döndürür veya ayarlar.

```csharp
public string Author { get; set; }
```

## Notlar

Olamaz`hükümsüz`.

Varsayılan boş dizgedir.

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
