---
title: NodeCollection.Item
second_title: Aspose.Words per .NET API Reference
description: NodeCollection proprietà. Recupera un nodo allindice specificato.
type: docs
weight: 20
url: /it/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Recupera un nodo all'indice specificato.

```csharp
public Node this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta di nodi. |

### Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 significa l'ultimo elemento, -2 significa il penultimo e così via.

Se indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento null.

Se indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento null.

### Esempi

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungi due sequenze e una forma come nodi secondari al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tieni presente che "CustomNodeId" non viene salvato in un file di output ed esiste solo durante la durata del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorrere la raccolta dei figli immediati del paragrafo,
// e stampa tutte le sequenze o le forme che troviamo all'interno.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Guarda anche

* class [Node](../../node/)
* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../nodecollection/)
* assemblea [Aspose.Words](../../../)


