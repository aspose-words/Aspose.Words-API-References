---
title: Document.update_actual_reference_marks method
linktitle: update_actual_reference_marks method
articleTitle: update_actual_reference_marks method
second_title: Aspose.Words for Python
description: "Document.update_actual_reference_marks method. Updates the [Footnote.actual_reference_mark](../../../aspose.words.notes/footnote/actual_reference_mark/) property of all footnotes and endnotes in the document."
type: docs
weight: 760
url: /python-net/aspose.words/document/update_actual_reference_marks/
---

## update_actual_reference_marks() {#default}

Updates the [Footnote.actual_reference_mark](../../../aspose.words.notes/footnote/actual_reference_mark/) property of all footnotes and endnotes in the document.



```python
def update_actual_reference_marks(self):
    ...
```

### Remarks

Updating fields ([Document.update_fields()](../update_fields/#default)) may be necessary to get the correct result.



### Examples

Shows how to get actual footnote reference mark.

```python
doc = aw.Document(file_name=MY_DIR + "Footnotes and endnotes.docx")
footnote = doc.get_child(aw.NodeType.FOOTNOTE, 1, True).as_footnote()
doc.update_fields()
doc.update_actual_reference_marks()
self.assertEqual("1", footnote.actual_reference_mark)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

