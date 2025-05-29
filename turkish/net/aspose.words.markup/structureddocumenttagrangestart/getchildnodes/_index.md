---
title: StructuredDocumentTagRangeStart.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: .NET için Aspose.Words
description: Belirtilen tiplerinize göre uyarlanmış dinamik bir alt düğüm koleksiyonu sağlayan StructuredDocumentTagRangeStart GetChildNodes metodunu keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Örnekler

StructuredDocumentTagRangeStart'ın alt düğümlerinin nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
