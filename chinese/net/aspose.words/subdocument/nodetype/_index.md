---
title: SubDocument.NodeType
second_title: Aspose.Words for .NET API 参考
description: SubDocument 财产. 返回SubDocument.
type: docs
weight: 10
url: /zh/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

返回SubDocument.

```csharp
public override NodeType NodeType { get; }
```

### 例子

演示如何访问主文档的子文档。

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// 该节点作为外部文档的引用，其内容无法访问。
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### 也可以看看

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* 命名空间 [Aspose.Words](../../subdocument/)
* 部件 [Aspose.Words](../../../)


