---
title: RevisionsView enumeration
linktitle: RevisionsView enumeration
articleTitle: RevisionsView enumeration
second_title: Aspose.Words for Python
description: "aspose.words.RevisionsView enumeration. Allows to specify whether to work with the original or revised version of a document."
type: docs
weight: 980
url: /python-net/aspose.words/revisionsview/
---

## RevisionsView enumeration

Allows to specify whether to work with the original or revised version of a document.


### Members

| Name | Description |
| --- | --- |
| ORIGINAL | Specifies original version of a document. |
| FINAL | Specifies revised version of a document. |

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

* module [aspose.words](../)

