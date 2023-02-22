---
title: GetChildNodes
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTagRangeStart method. Returns a live collection of child nodes that match the specified types in C#.
type: docs
weight: 210
url: /net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Returns a live collection of child nodes that match the specified types.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assembly [Aspose.Words](../../../)
