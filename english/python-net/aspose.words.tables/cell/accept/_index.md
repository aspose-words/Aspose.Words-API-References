---
title: Cell.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "Cell.accept method. Accepts a visitor."
type: docs
weight: 130
url: /python-net/aspose.words.tables/cell/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_cell_start()](../../../aspose.words/documentvisitor/visit_cell_start/#cell), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all child nodes of the section
and calls [DocumentVisitor.visit_cell_end()](../../../aspose.words/documentvisitor/visit_cell_end/#cell) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

