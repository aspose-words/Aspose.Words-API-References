---
title: BuiltInDocumentProperties.hyperlinks_changed property
linktitle: hyperlinks_changed property
articleTitle: hyperlinks_changed property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlinks_changed property. Indicates whether hyperlinks in a document were changed."
type: docs
weight: 140
url: /python-net/aspose.words.properties/builtindocumentproperties/hyperlinks_changed/
---

## BuiltInDocumentProperties.hyperlinks_changed property

Indicates whether hyperlinks in a document were changed.


```python
@property
def hyperlinks_changed(self) -> bool:
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

