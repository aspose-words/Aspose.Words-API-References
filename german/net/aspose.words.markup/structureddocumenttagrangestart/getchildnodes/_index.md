---
title: StructuredDocumentTagRangeStart.GetChildNodes
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagRangeStart methode. Gibt eine LiveSammlung untergeordneter Knoten zurück die den angegebenen Typen entsprechen.
type: docs
weight: 210
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Gibt eine Live-Sammlung untergeordneter Knoten zurück, die den angegebenen Typen entsprechen.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

### Beispiele

Zeigt, wie untergeordnete Knoten von StructuredDocumentTagRangeStart abgerufen werden.

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

### Siehe auch

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* Montage [Aspose.Words](../../../)


