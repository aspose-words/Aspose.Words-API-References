---
title: StructuredDocumentTagRangeStart.remove_self_only method
linktitle: remove_self_only method
articleTitle: remove_self_only method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.remove_self_only method. Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree."
type: docs
weight: 240
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/remove_self_only/
---

## remove_self_only() {#default}

Removes this range start and appropriate range end nodes of the structured document tag,
but keeps its content inside the document tree.


```python
def remove_self_only(self):
    ...
```

### Examples

Shows how to create/remove structured document tag and its content (InsertStructuredDocumentTagRanges).

```python
def insert_structured_document_tag_ranges(self, doc):
    range_start = aw.markup.StructuredDocumentTagRangeStart(doc, aw.markup.SdtType.PLAIN_TEXT)
    range_end = aw.markup.StructuredDocumentTagRangeEnd(doc, range_start.id)
    doc.first_section.body.insert_before(range_start, doc.first_section.body.first_paragraph)
    doc.last_section.body.insert_after(range_end, doc.first_section.body.first_paragraph)
    return range_start
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

