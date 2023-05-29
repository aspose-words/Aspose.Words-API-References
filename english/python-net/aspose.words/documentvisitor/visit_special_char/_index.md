---
title: DocumentVisitor.visit_special_char method
linktitle: visit_special_char method
articleTitle: visit_special_char method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_special_char method. Called when a [SpecialChar](../../specialchar/) node is encountered in the document."
type: docs
weight: 430
url: /python-net/aspose.words/documentvisitor/visit_special_char/
---

## visit_special_char(special_char) {#specialchar}

Called when a [SpecialChar](../../specialchar/) node is encountered in the document.



```python
def visit_special_char(self, special_char: aspose.words.SpecialChar):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| special_char | [SpecialChar](../../specialchar/) |  |

This method is not be called for generic control characters (see [ControlChar](../../controlchar/)) that can be present in the document.



### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

