---
title: versions_count property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the number of document versions that was stored in the DOC document."
type: docs
weight: 440
url: /python-net/aspose.words/document/versions_count/
---

## Document.versions_count property

Gets the number of document versions that was stored in the DOC document.

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports
versions only for DOC files.

This property allows to detect if there were document versions stored in this document
before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions.
If you save this document using Aspose.Words, the document will be saved without versions.




### Examples

Shows how to work with the versions count feature of older Microsoft Word documents.

```python
doc = aw.Document(MY_DIR + "Versions.doc")

# We can read this property of a document, but we cannot preserve it while saving.
self.assertEqual(4, doc.versions_count)

doc.save(ARTIFACTS_DIR + "Document.versions_count.doc")
doc = aw.Document(ARTIFACTS_DIR + "Document.versions_count.doc")

self.assertEqual(0, doc.versions_count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

