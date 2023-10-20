---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: Comment Author mülk. Bir yorumun yazar adını döndürür veya ayarlar C#'da.
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

Varsayılan boş dizedir.

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
