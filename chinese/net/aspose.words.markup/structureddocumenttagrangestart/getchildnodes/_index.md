---
title: GetChildNodes
second_title: Aspose.Words for .NET API 参考
description: 返回与指定类型匹配的子节点的实时集合
type: docs
weight: 210
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

返回与指定类型匹配的子节点的实时集合。

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

### 例子

展示如何获取 StructuredDocumentTagRangeStart 的子节点。

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

### 也可以看看

* class [NodeCollection](../../../aspose.words/nodecollection)
* enum [NodeType](../../../aspose.words/nodetype)
* class [StructuredDocumentTagRangeStart](../../structureddocumenttagrangestart)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttagrangestart)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
