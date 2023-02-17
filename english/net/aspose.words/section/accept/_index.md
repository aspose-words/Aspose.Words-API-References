---
title: Section.Accept
second_title: Aspose.Words for .NET API Reference
description: Section method. Accepts a visitor in C#.
type: docs
weight: 70
url: /net/aspose.words/section/accept/
---
## Section.Accept method

Accepts a visitor.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The visitor that will visit the nodes. |

### Return Value

True if all nodes were visited; false if [`DocumentVisitor`](../../documentvisitor/) stopped the operation before visiting all nodes.

## Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [`DocumentVisitor`](../../documentvisitor/).

For more info see the Visitor design pattern.

Calls [`VisitSectionStart`](../../documentvisitor/visitsectionstart/), then calls [`Accept`](../../node/accept/) for all child nodes of the section and calls [`VisitSectionEnd`](../../documentvisitor/visitsectionend/) at the end.

### See Also

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* namespace [Aspose.Words](../../section/)
* assembly [Aspose.Words](../../../)
