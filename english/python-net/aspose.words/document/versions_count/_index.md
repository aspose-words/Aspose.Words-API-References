---
title: Document.versions_count property
linktitle: versions_count property
articleTitle: versions_count property
second_title: Aspose.Words for Python
description: "Document.versions_count property. Gets the number of document versions that was stored in the DOC document."
type: docs
weight: 480
url: /python-net/aspose.words/document/versions_count/
---

## Document.versions_count property

Gets the number of document versions that was stored in the DOC document.


```python
@property
def versions_count(self) -> int:
    ...

```

### Remarks

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports
versions only for DOC files.

This property allows to detect if there were document versions stored in this document
before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions.
If you save this document using Aspose.Words, the document will be saved without versions.




### Examples

Shows how to work with the versions count feature of older Microsoft Word documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Versions.doc')
# We can read this property of a document, but we cannot preserve it while saving.
self.assertEqual(4, doc.versions_count)
doc.save(file_name=ARTIFACTS_DIR + 'Document.VersionsCount.doc')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.VersionsCount.doc')
self.assertEqual(0, doc.versions_count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

