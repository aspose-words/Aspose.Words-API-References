---
title: StructuredDocumentTagRangeStart.ChildNodes
linktitle: ChildNodes
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTagRangeStart property. Gets all nodes between this range start node and the range end node in C#.
type: docs
weight: 20
url: /net/aspose.words.markup/structureddocumenttagrangestart/childnodes/
---
## StructuredDocumentTagRangeStart.ChildNodes property

Gets all nodes between this range start node and the range end node.

```csharp
public NodeCollection ChildNodes { get; }
```

## Examples

Shows how to get child nodes of StructuredDocumentTagRangeStart.

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

### See Also

* class [NodeCollection](../../../aspose.words/nodecollection/)
* class [StructuredDocumentTagRangeStart](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assembly [Aspose.Words](../../../)
