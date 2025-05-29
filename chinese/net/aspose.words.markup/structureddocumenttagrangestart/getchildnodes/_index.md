---
title: StructuredDocumentTagRangeStart.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words for .NET
description: 发现 StructuredDocumentTagRangeStart GetChildNodes 方法，该方法提供了根据您指定的类型定制的子节点的动态集合。
type: docs
weight: 220
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

返回与指定类型匹配的子节点的实时集合。

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## 例子

展示如何获取 StructuredDocumentTagRangeStart 的子节点。

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

### 也可以看看

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
