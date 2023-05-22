---
title: Document.revisions_view property
linktitle: revisions_view property
articleTitle: revisions_view property
second_title: Aspose.Words for Python
description: "Document.revisions_view property. Gets or sets a value indicating whether to work with the original or revised version of a document."
type: docs
weight: 360
url: /python-net/aspose.words/document/revisions_view/
---

## Document.revisions_view property

Gets or sets a value indicating whether to work with the original or revised version of a document.

The default value is ****.



### Examples

Shows how to switch between the revised and the original view of a document.

```python
doc = aw.Document(MY_DIR + "Revisions at list levels.docx")
doc.update_list_labels()

paragraphs = doc.first_section.body.paragraphs
self.assertEqual("1.", paragraphs[0].list_label.label_string)
self.assertEqual("a.", paragraphs[1].list_label.label_string)
self.assertEqual("", paragraphs[2].list_label.label_string)

# View the document object as if all the revisions are accepted. Currently supports list labels.
doc.revisions_view = aw.RevisionsView.FINAL

self.assertEqual("", paragraphs[0].list_label.label_string)
self.assertEqual("1.", paragraphs[1].list_label.label_string)
self.assertEqual("a.", paragraphs[2].list_label.label_string)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

