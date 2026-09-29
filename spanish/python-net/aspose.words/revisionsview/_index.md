---
title: RevisionsView enumeration
linktitle: RevisionsView enumeration
articleTitle: RevisionsView enumeration
second_title: Aspose.Words for Python
description: "aspose.words.RevisionsView enumeration. Allows to specify whether to work with the original or revised version of a document."
type: docs
weight: 1100
url: /es/python-net/aspose.words/revisionsview/
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
doc = aw.Document(file_name=MY_DIR + 'Revisions at list levels.docx')
doc.update_list_labels()
paragraphs = doc.first_section.body.paragraphs
self.assertEqual('1.', paragraphs[0].list_label.label_string)
self.assertEqual('a.', paragraphs[1].list_label.label_string)
self.assertEqual('', paragraphs[2].list_label.label_string)
# Ver el objeto documento como si todas las revisiones estuvieran aceptadas. Actualmente soporta etiquetas de lista.
doc.revisions_view = aw.RevisionsView.FINAL
self.assertEqual('', paragraphs[0].list_label.label_string)
self.assertEqual('1.', paragraphs[1].list_label.label_string)
self.assertEqual('a.', paragraphs[2].list_label.label_string)
```

### See Also

* module [aspose.words](../)

