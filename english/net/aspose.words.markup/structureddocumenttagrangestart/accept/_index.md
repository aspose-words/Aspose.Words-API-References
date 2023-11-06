---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: StructuredDocumentTagRangeStart Accept method. Accepts a visitor in C#.
type: docs
weight: 200
url: /net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Accepts a visitor.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The visitor that will visit the nodes. |

### Return Value

True if all nodes were visited; false if [`DocumentVisitor`](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.

## Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [`DocumentVisitor`](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

### See Also

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
