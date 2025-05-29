---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: Alt düğümler üzerinde sorunsuz yineleme için CompositeNode GetEnumerator metodunu keşfedin. Bu güçlü özellik ile kodlama verimliliğinizi artırın!
type: docs
weight: 120
url: /tr/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar.

```csharp
public IEnumerator<Node> GetEnumerator()
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

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
