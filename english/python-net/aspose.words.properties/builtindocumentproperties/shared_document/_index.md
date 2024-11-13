---
title: BuiltInDocumentProperties.shared_document property
linktitle: shared_document property
articleTitle: shared_document property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.shared_document property. Indicates whether the document is a shared document."
type: docs
weight: 280
url: /python-net/aspose.words.properties/builtindocumentproperties/shared_document/
---

## BuiltInDocumentProperties.shared_document property

Indicates whether the document is a shared document.


```python
@property
def shared_document(self) -> bool:
    ...

```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to get extended properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Extended properties.docx')
self.assertTrue(doc.built_in_document_properties.scale_crop)
self.assertTrue(doc.built_in_document_properties.shared_document)
self.assertTrue(doc.built_in_document_properties.hyperlinks_changed)
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

