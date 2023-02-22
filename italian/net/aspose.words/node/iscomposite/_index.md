---
title: Node.IsComposite
second_title: Aspose.Words per .NET API Reference
description: Node proprietà. Restituisce vero se questo nodo può contenere altri nodi.
type: docs
weight: 30
url: /it/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

Restituisce vero se questo nodo può contenere altri nodi.

```csharp
public virtual bool IsComposite { get; }
```

### Valore della proprietà

Questo metodo restituisce false poiché Node non può avere nodi figlio.

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

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../node/)
* assemblea [Aspose.Words](../../../)


