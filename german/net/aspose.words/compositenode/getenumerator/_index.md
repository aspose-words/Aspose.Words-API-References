---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompositeNode GetEnumerator-Methode für die nahtlose Iteration über untergeordnete Knoten. Steigern Sie Ihre Programmiereffizienz mit dieser leistungsstarken Funktion!
type: docs
weight: 120
url: /de/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Beispiele

Zeigt, wie alle Kommentare und Antworten eines Dokuments gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Wenn ein Kommentar keinen Vorgänger hat, handelt es sich um einen Kommentar der obersten Ebene und nicht um einen Kommentar vom Typ „Antwort“.
// Alle Kommentare der obersten Ebene zusammen mit allen möglichen Antworten ausdrucken.
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

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
