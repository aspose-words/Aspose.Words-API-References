---
title: Node.NextSibling
linktitle: NextSibling
articleTitle: NextSibling
second_title: Aspose.Words per .NET
description: Scopri la proprietà Node NextSibling per accedere facilmente al nodo successivo nel tuo DOM. Migliora le tue competenze JavaScript e semplifica la tua programmazione oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words/node/nextsibling/
---
## Node.NextSibling property

Ottiene il nodo immediatamente successivo a questo nodo.

```csharp
public Node NextSibling { get; }
```

## Osservazioni

Se non c'è un nodo successivo, un`null` viene restituito.

## Esempi

Mostra come utilizzare la proprietà NextSibling di un nodo per enumerare i suoi figli immediati.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

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

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
