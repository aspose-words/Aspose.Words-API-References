---
title: StructuredDocumentTag.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.accept method. Accepts a visitor."
type: docs
weight: 330
url: /python-net/aspose.words.markup/structureddocumenttag/accept/
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




Calls [DocumentVisitor.visit_structured_document_tag_start()](../../../aspose.words/documentvisitor/visit_structured_document_tag_start/#structureddocumenttag), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all
child nodes of the smart tag and calls [DocumentVisitor.visit_structured_document_tag_end()](../../../aspose.words/documentvisitor/visit_structured_document_tag_end/#structureddocumenttag) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

