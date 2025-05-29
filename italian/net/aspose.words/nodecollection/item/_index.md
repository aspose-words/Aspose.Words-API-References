---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi a qualsiasi nodo senza problemi con la proprietà NodeCollection Item. Recupera rapidamente i nodi in base all'indice per una gestione dei dati fluida e prestazioni migliorate.
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

## Osservazioni

L'indice è basato sullo zero.

Sono consentiti indici negativi che indicano l'accesso dalla parte posteriore della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, viene restituito un riferimento null.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, viene restituito un riferimento null.

## Esempi

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungere due sequenze e una forma come nodi figlio al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo per la durata del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorrere la raccolta di elementi figlio immediati del paragrafo,
// e stampare tutte le sequenze o le forme che troviamo al suo interno.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
