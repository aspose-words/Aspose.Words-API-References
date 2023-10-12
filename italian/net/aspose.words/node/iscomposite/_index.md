---
title: Node.IsComposite
second_title: Aspose.Words per .NET API Reference
description: Node proprietà. RestituisceVERO se questo nodo può contenere altri nodi.
type: docs
weight: 30
url: /it/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

Restituisce`VERO` se questo nodo può contenere altri nodi.

```csharp
public virtual bool IsComposite { get; }
```

### Valore della proprietà

Questo metodo ritorna`falso` COME[`Node`](../) non può avere nodi figli.

### Esempi

Mostra come attraversare l'albero dei nodi figlio di un nodo composito.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Qualsiasi nodo che può contenere nodi secondari, come il documento stesso, è composito.
    Assert.True(doc.IsComposite);

    // Richiama la funzione ricorsiva che esaminerà e stamperà tutti i nodi figli di un nodo composito.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Attraversa ricorsivamente un albero di nodi durante la stampa del tipo di ciascun nodo
/// con un rientro che dipende dalla profondità e dal contenuto di tutti i nodi in linea.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Ricorsione nel nodo se è un nodo composito. Altrimenti, stampa il suo contenuto se è un nodo in linea.
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


