---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 90
url: /python-net/aspose.words/node/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.




### Returns

True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.


### See Also

* module [aspose.words](../../)
* class [Node](../)

