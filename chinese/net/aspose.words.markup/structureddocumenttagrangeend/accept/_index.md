---
title: StructuredDocumentTagRangeEnd.Accept
linktitle: Accept
articleTitle: Accept
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTagRangeEnd Accept 方法. 接受访客 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；假如果[`DocumentVisitor`](../../../aspose.words/documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举该节点及其所有子节点。每个节点调用相应的方法[`DocumentVisitor`](../../../aspose.words/documentvisitor/)。

有关更多信息，请参阅访客设计模式。

### 也可以看看

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeEnd](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
