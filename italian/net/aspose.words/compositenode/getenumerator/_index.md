---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words per .NET
description: Esplora il metodo CompositeNode GetEnumerator per un'iterazione fluida sui nodi figlio. Migliora l'efficienza della tua programmazione con questa potente funzionalità!
type: docs
weight: 120
url: /it/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Esempi

Mostra come stampare tutti i commenti di un documento e le relative risposte.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Se un commento non ha antenati, si tratta di un commento di "livello superiore" e non di un commento di tipo risposta.
// Stampa tutti i commenti di primo livello insieme alle eventuali risposte.
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

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
