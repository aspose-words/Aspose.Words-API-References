---
title: StructuredDocumentTagRangeEnd.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeEnd.accept method. Accepts a visitor."
type: docs
weight: 40
url: /python-net/aspose.words.markup/structureddocumenttagrangeend/accept/
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




### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeEnd](../)

