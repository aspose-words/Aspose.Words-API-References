---
title: Footnote.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words per .NET
description: Scopri la proprietà Footnote NodeType che recupera in modo efficiente le note a piè di pagina, migliorando la chiarezza e l'organizzazione del tuo documento.
type: docs
weight: 50
url: /it/net/aspose.words.notes/footnote/nodetype/
---
## Footnote.NodeType property

RestituisceFootnote .

```csharp
public override NodeType NodeType { get; }
```

## Esempi

Mostra come attraversare l'albero dei nodi figlio di un nodo composito.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Qualsiasi nodo che può contenere nodi figlio, come il documento stesso, è composito.
    Assert.True(doc.IsComposite);

    // Richiama la funzione ricorsiva che esaminerà e stamperà tutti i nodi figlio di un nodo composito.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Attraversa ricorsivamente un albero di nodi mentre stampa il tipo di ciascun nodo
/// con un rientro che dipende dalla profondità e dal contenuto di tutti i nodi in linea.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Ricorsiva nel nodo se è un nodo composito. Altrimenti, ne stampa il contenuto se è un nodo inline.
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Footnote](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
