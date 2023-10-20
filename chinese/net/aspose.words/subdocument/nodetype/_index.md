---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: 用于 .NET 的 Aspose.Words
description: SubDocument NodeType 财产. 返回节点类型.子文档 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

返回**节点类型.子文档**

```csharp
public override NodeType NodeType { get; }
```

## 例子

显示如何访问主控文档的子文档。

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// 该节点作为外部文档的引用，不能访问其内容。
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### 也可以看看

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
