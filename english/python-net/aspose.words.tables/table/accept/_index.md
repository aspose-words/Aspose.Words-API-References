---
title: Table.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "Table.accept method. Accepts a visitor."
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

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_table_start()](../../../aspose.words/documentvisitor/visit_table_start/#table), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all child nodes of the section
and calls [DocumentVisitor.visit_table_end()](../../../aspose.words/documentvisitor/visit_table_end/#table) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

