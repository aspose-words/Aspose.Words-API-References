---
title: StructuredDocumentTagRangeStart.ChildNodes
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagRangeStart eigendom. Ruft alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs ab.
type: docs
weight: 20
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/childnodes/
---
## StructuredDocumentTagRangeStart.ChildNodes property

Ruft alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs ab.

```csharp
public NodeCollection ChildNodes { get; }
```

### Beispiele

Zeigt, wie untergeordnete Knoten von StructuredDocumentTagRangeStart abgerufen werden.

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

### Siehe auch

* class [NodeCollection](../../../aspose.words/nodecollection/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* Montage [Aspose.Words](../../../)


