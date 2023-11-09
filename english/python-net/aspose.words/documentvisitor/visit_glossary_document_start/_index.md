---
title: DocumentVisitor.visit_glossary_document_start method
linktitle: visit_glossary_document_start method
articleTitle: visit_glossary_document_start method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_glossary_document_start method. Called when enumeration of a glossary document has started."
type: docs
weight: 250
url: /python-net/aspose.words/documentvisitor/visit_glossary_document_start/
---

## visit_glossary_document_start(glossary) {#glossarydocument}

Called when enumeration of a glossary document has started.


```python
def visit_glossary_document_start(self, glossary: aspose.words.buildingblocks.GlossaryDocument):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) | The object that is being visited. |

### Remarks

Note: A glossary document node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
glossary document, you need to call [GlossaryDocument.accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/#documentvisitor).





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

