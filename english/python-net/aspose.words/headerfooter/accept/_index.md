---
title: HeaderFooter.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "HeaderFooter.accept method. Accepts a visitor."
type: docs
weight: 70
url: /python-net/aspose.words/headerfooter/accept/
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




Calls [DocumentVisitor.visit_header_footer_start()](../../documentvisitor/visit_header_footer_start/#headerfooter), then calls [Node.accept()](../../node/accept/#documentvisitor) for all child nodes of the section
and calls [DocumentVisitor.visit_header_footer_end()](../../documentvisitor/visit_header_footer_end/#headerfooter) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

