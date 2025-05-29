---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: 发现有效返回 SubDocument 数据的 SubDocument NodeType 属性，增强您的文档管理和处理能力。
type: docs
weight: 10
url: /zh/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

返回SubDocument.

```csharp
public override NodeType NodeType { get; }
```

## 例子

显示如何访问主文档的子文档。

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// 此节点作为外部文档的引用，其内容无法访问。
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### 也可以看看

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
