---
title: DocumentVisitor.visit_glossary_document_end method
linktitle: visit_glossary_document_end method
articleTitle: visit_glossary_document_end method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_glossary_document_end method. Called when enumeration of a glossary document has ended."
type: docs
weight: 240
url: /python-net/aspose.words/documentvisitor/visit_glossary_document_end/
---

## visit_glossary_document_end(glossary) {#glossarydocument}

Called when enumeration of a glossary document has ended.


```python
def visit_glossary_document_end(self, glossary: aspose.words.buildingblocks.GlossaryDocument):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) |  |

Note: A glossary document node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
glossary document, you need to call [GlossaryDocument.accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/#documentvisitor).





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

