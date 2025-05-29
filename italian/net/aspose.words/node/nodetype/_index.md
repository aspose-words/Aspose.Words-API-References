---
title: Node.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words per .NET
description: Scopri la proprietà Node NodeType per identificare facilmente i tipi di nodo nella tua applicazione, migliorando l'efficienza dello sviluppo e la chiarezza del codice.
type: docs
weight: 50
url: /it/net/aspose.words/node/nodetype/
---
## Node.NodeType property

Ottiene il tipo di questo nodo.

```csharp
public abstract NodeType NodeType { get; }
```

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

Mostra come rimuovere tutti i nodi figlio di un tipo specifico da un nodo composito.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Salva il nodo fratello successivo come variabile nel caso in cui volessimo spostarci su di esso dopo aver eliminato questo nodo.
    Node nextNode = curNode.NextSibling;

    // Il corpo di una sezione può contenere nodi Paragrafo e Tabella.
    // Se il nodo è una tabella, rimuoverla dal padre.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
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

* enum [NodeType](../../nodetype/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
