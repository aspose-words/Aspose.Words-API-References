---
title: DocumentVisitor.visit_field_start method
linktitle: visit_field_start method
articleTitle: visit_field_start method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_field_start method. Called when a field starts in the document."
type: docs
weight: 200
url: /python-net/aspose.words/documentvisitor/visit_field_start/
---

## visit_field_start(field_start) {#fieldstart}

Called when a field starts in the document.


```python
def visit_field_start(self, field_start: aspose.words.fields.FieldStart):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_start | [FieldStart](../../../aspose.words.fields/fieldstart/) | The object that is being visited. |

### Remarks

A field in a Word document consists of a field code and field value.

For example, a field that displays a page number can be represented as follows:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

The field separator separates field code from field value in the document. Note that some 
fields have only field code and do not have field separator and field value.

Fields can be nested.




### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

