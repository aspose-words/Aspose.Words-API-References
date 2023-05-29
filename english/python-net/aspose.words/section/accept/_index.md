---
title: Section.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "Section.accept method. Accepts a visitor."
type: docs
weight: 70
url: /python-net/aspose.words/section/accept/
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




Calls [DocumentVisitor.visit_section_start()](../../documentvisitor/visit_section_start/#section), then calls [Node.accept()](../../node/accept/#documentvisitor) for all child nodes of the section
and calls [DocumentVisitor.visit_section_end()](../../documentvisitor/visit_section_end/#section) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words](../../)
* class [Section](../)

