---
title: CommentRangeEnd.NodeType
second_title: Aspose.Words per .NET API Reference
description: CommentRangeEnd proprietà. RestituisceCommentRangeEnd .
type: docs
weight: 30
url: /it/net/aspose.words/commentrangeend/nodetype/
---
## CommentRangeEnd.NodeType property

RestituisceCommentRangeEnd .

```csharp
public override NodeType NodeType { get; }
```

### Esempi

Mostra come attraversare l'albero dei nodi figlio di un nodo composito.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Qualsiasi nodo che può contenere nodi figlio, come il documento stesso, è composto.
    Assert.True(doc.IsComposite);

    // Richiama la funzione ricorsiva che passerà attraverso e stamperà tutti i nodi figlio di un nodo composito.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Attraversa ricorsivamente un albero di nodi durante la stampa del tipo di ciascun nodo
/// con un rientro a seconda della profondità e del contenuto di tutti i nodi inline.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Ricorre nel nodo se si tratta di un nodo composito. In caso contrario, stampa il suo contenuto se si tratta di un nodo inline.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### Guarda anche

* enum [NodeType](../../nodetype/)
* class [CommentRangeEnd](../)
* spazio dei nomi [Aspose.Words](../../commentrangeend/)
* assemblea [Aspose.Words](../../../)


