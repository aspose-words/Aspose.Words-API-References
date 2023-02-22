---
title: StructuredDocumentTagRangeStart.ChildNodes
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagRangeStart proprietà. Ottiene tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dellintervallo.
type: docs
weight: 20
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/childnodes/
---
## StructuredDocumentTagRangeStart.ChildNodes property

Ottiene tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dell'intervallo.

```csharp
public NodeCollection ChildNodes { get; }
```

### Esempi

Mostra come ottenere i nodi figlio di StructuredDocumentTagRangeStart.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Child nodes count: {tag.ChildNodes.Count}\n");

foreach (Node node in tag.ChildNodes)
    Console.WriteLine($"\t|Child node type: {node.NodeType}");

foreach (Node node in tag.GetChildNodes(NodeType.Run, true))
    Console.WriteLine($"\t|Child node text: {node.GetText()}");
```

### Guarda anche

* class [NodeCollection](../../../aspose.words/nodecollection/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assemblea [Aspose.Words](../../../)


