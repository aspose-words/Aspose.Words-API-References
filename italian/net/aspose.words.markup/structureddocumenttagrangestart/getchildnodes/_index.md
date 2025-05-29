---
title: StructuredDocumentTagRangeStart.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words per .NET
description: Scopri il metodo GetChildNodes di StructuredDocumentTagRangeStart, che fornisce una raccolta dinamica di nodi figlio personalizzati in base ai tipi specificati.
type: docs
weight: 220
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Restituisce una raccolta live di nodi figlio che corrispondono ai tipi specificati.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Esempi

Mostra come ottenere i nodi figlio di StructuredDocumentTagRangeStart.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Child nodes count: {tag.GetChildNodes(NodeType.Any, false).Count}\n");

foreach (Node node in tag.GetChildNodes(NodeType.Any, false))
    Console.WriteLine($"\t|Child node type: {node.NodeType}");

foreach (Node node in tag.GetChildNodes(NodeType.Run, true))
    Console.WriteLine($"\t|Child node text: {node.GetText()}");
```

### Guarda anche

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
