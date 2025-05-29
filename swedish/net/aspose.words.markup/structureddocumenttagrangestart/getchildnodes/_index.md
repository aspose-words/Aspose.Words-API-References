---
title: StructuredDocumentTagRangeStart.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words för .NET
description: Upptäck metoden StructuredDocumentTagRangeStart GetChildNodes, som tillhandahåller en dynamisk samling av underordnade noder anpassade till dina angivna typer.
type: docs
weight: 220
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Returnerar en live-samling av underordnade noder som matchar de angivna typerna.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Exempel

Visar hur man hämtar underordnade noder till StructuredDocumentTagRangeStart.

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

### Se även

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
