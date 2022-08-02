---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 350
url: /python-net/aspose.words.tables/table/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.




Calls DocumentVisitor.VisitTableStart, then calls Accept for all child nodes of the section
and calls DocumentVisitor.VisitTableEnd at the end.


### Returns

True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

