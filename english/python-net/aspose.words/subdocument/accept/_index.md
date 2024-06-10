---
title: SubDocument.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "SubDocument.accept method. Accepts a visitor."
type: docs
weight: 20
url: /python-net/aspose.words/subdocument/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.




### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words](../../)
* class [SubDocument](../)

