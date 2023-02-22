---
title: StructuredDocumentTagRangeStart.GetChildNodes
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagRangeStart método. Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados.
type: docs
weight: 210
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

### Ejemplos

Muestra cómo obtener nodos secundarios de StructuredDocumentTagRangeStart.

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

### Ver también

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* asamblea [Aspose.Words](../../../)


