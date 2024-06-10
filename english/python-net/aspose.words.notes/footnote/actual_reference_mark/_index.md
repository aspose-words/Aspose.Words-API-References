---
title: Footnote.actual_reference_mark property
linktitle: actual_reference_mark property
articleTitle: actual_reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.actual_reference_mark property. Gets the actual text of the reference mark displayed in the document for this footnote."
type: docs
weight: 20
url: /python-net/aspose.words.notes/footnote/actual_reference_mark/
---

## Footnote.actual_reference_mark property

Gets the actual text of the reference mark displayed in the document for this footnote.


```python
@property
def actual_reference_mark(self) -> str:
    ...

```

### Remarks

To initially populate values of this property for all reference marks of the document, or to update
the values after changes in the document that might affect the reference marks, you must execute the
[Document.update_actual_reference_marks()](../../../aspose.words/document/update_actual_reference_marks/#default) method.
Updating fields ([Document.update_fields()](../../../aspose.words/document/update_fields/#default)) may also be necessary to get the correct result.



### Examples

Shows how to get actual footnote reference mark.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
footnote = doc.get_child(aw.NodeType.FOOTNOTE, 1, True).as_footnote()
doc.update_fields()
doc.update_actual_reference_marks()
self.assertEqual('1', footnote.actual_reference_mark)
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

