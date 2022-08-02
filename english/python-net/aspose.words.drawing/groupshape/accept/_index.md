---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/groupshape/accept/
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




Calls [DocumentVisitor.visit_group_shape_start()](../../../aspose.words/documentvisitor/visit_group_shape_start/#groupshape), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all 
child shapes of this group shape and calls [DocumentVisitor.visit_group_shape_end()](../../../aspose.words/documentvisitor/visit_group_shape_end/#groupshape) at the end.



### Returns

True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.drawing](../../)
* class [GroupShape](../)

