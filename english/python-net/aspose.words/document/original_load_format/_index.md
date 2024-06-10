---
title: Document.original_load_format property
linktitle: original_load_format property
articleTitle: original_load_format property
second_title: Aspose.Words for Python
description: "Document.original_load_format property. Gets the format of the original document that was loaded into this object."
type: docs
weight: 310
url: /python-net/aspose.words/document/original_load_format/
---

## Document.original_load_format property

Gets the format of the original document that was loaded into this object.


```python
@property
def original_load_format(self) -> aspose.words.LoadFormat:
    ...

```

### Remarks

If you created a new blank document, returns the [LoadFormat.DOC](../../loadformat/#DOC) value.




### Examples

Shows how to retrieve details of a document's load operation.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
self.assertEqual(MY_DIR + 'Document.docx', doc.original_file_name)
self.assertEqual(aw.LoadFormat.DOCX, doc.original_load_format)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

