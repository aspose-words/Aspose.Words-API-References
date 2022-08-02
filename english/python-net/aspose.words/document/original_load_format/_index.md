---
title: original_load_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the format of the original document that was loaded into this object."
type: docs
weight: 280
url: /python-net/aspose.words/document/original_load_format/
---

## Document.original_load_format property

Gets the format of the original document that was loaded into this object.

If you created a new blank document, returns the [LoadFormat.DOC](../../loadformat/#DOC) value.




### Examples

Shows how to retrieve details of a document's load operation.

```python
doc = aw.Document(MY_DIR + "Document.docx")

self.assertEqual(MY_DIR + "Document.docx", doc.original_file_name)
self.assertEqual(aw.LoadFormat.DOCX, doc.original_load_format)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

