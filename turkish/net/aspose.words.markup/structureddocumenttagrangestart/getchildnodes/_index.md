---
title: StructuredDocumentTagRangeStart.GetChildNodes
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagRangeStart yöntem. Belirtilen türlerle eşleşen canlı bir alt düğüm koleksiyonu döndürür.
type: docs
weight: 210
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Belirtilen türlerle eşleşen canlı bir alt düğüm koleksiyonu döndürür.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

### Örnekler

StructuredDocumentTagRangeStart alt düğümlerinin nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* toplantı [Aspose.Words](../../../)


