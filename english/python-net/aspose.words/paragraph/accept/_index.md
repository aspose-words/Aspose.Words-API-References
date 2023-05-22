---
title: Paragraph.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "Paragraph.accept method. Accepts a visitor."
type: docs
weight: 230
url: /python-net/aspose.words/paragraph/accept/
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

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_paragraph_start()](../../documentvisitor/visit_paragraph_start/#paragraph), then calls [Node.accept()](../../node/accept/#documentvisitor) for all child nodes
of the paragraph and calls [DocumentVisitor.visit_paragraph_end()](../../documentvisitor/visit_paragraph_end/#paragraph) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

