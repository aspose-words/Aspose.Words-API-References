---
title: Document.glossary_document property
linktitle: glossary_document property
articleTitle: glossary_document property
second_title: Aspose.Words for Python
description: "Document.glossary_document property. Gets or sets the glossary document within this document or template"
type: docs
weight: 170
url: /python-net/aspose.words/document/glossary_document/
---

## Document.glossary_document property

Gets or sets the glossary document within this document or template. A glossary document is a storage
for AutoText, AutoCorrect and Building Block entries defined in a document.


```python
@property
def glossary_document(self) -> aspose.words.buildingblocks.GlossaryDocument:
    ...

@glossary_document.setter
def glossary_document(self, value: aspose.words.buildingblocks.GlossaryDocument):
    ...

```

### Remarks

This property returns ``None`` if the document does not have a glossary document.

You can add a glossary document to a document by creating a
[GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) object and assigning to this property.




### See Also

* module [aspose.words](../../)
* class [Document](../)
* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)

