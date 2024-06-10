---
title: Run.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "Run.accept method. Accepts a visitor."
type: docs
weight: 60
url: /python-net/aspose.words/run/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../documentvisitor/) | The visitor that will visit the node. |

### Remarks

Calls [DocumentVisitor.visit_run()](../../documentvisitor/visit_run/#run).

For more info see the Visitor design pattern.




### Returns

``False`` if the visitor requested the enumeration to stop.


### See Also

* module [aspose.words](../../)
* class [Run](../)

