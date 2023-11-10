---
title: FieldEnd.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "FieldEnd.accept method. Accepts a visitor."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldend/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) | The visitor that will visit the node. |

### Remarks

Calls [DocumentVisitor.visit_field_end()](../../../aspose.words/documentvisitor/visit_field_end/#fieldend).

For more info see the Visitor design pattern.




### Returns

**False** if the visitor requested the enumeration to stop.


### See Also

* module [aspose.words.fields](../../)
* class [FieldEnd](../)

