---
title: DocumentVisitor.visit_field_separator method
linktitle: visit_field_separator method
articleTitle: visit_field_separator method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_field_separator method. Called when a field separator is encountered in the document."
type: docs
weight: 190
url: /python-net/aspose.words/documentvisitor/visit_field_separator/
---

## visit_field_separator(field_separator) {#fieldseparator}

Called when a field separator is encountered in the document.


```python
def visit_field_separator(self, field_separator: aspose.words.fields.FieldSeparator):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_separator | [FieldSeparator](../../../aspose.words.fields/fieldseparator/) | The object that is being visited. |

### Remarks

The field separator separates field code from field value in the document. Note that some 
fields have only field code and do not have field separator and field value.

For more info see [DocumentVisitor.visit_field_start()](../visit_field_start/#fieldstart)





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

