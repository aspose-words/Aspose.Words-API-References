---
title: BuiltInDocumentProperties.scale_crop property
linktitle: scale_crop property
articleTitle: scale_crop property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.scale_crop property. Indicates whether document thumbnail is cropped or scaled to fit the display."
type: docs
weight: 260
url: /python-net/aspose.words.properties/builtindocumentproperties/scale_crop/
---

## BuiltInDocumentProperties.scale_crop property

Indicates whether document thumbnail is cropped or scaled to fit the display.


```python
@property
def scale_crop(self) -> bool:
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

