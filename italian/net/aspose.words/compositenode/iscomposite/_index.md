---
title: CompositeNode.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsComposite di CompositeNode. Verifica facilmente se un nodo supporta nodi figlio per una gestione avanzata della struttura dati.
type: docs
weight: 40
url: /it/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Restituisce`VERO` poiché questo nodo può avere nodi figlio.

```csharp
public override bool IsComposite { get; }
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

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
