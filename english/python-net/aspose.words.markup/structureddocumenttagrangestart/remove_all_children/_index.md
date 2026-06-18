---
title: StructuredDocumentTagRangeStart.remove_all_children method
linktitle: remove_all_children method
articleTitle: remove_all_children method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.remove_all_children method. Removes all the nodes between this range start node and the range end node."
type: docs
weight: 230
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/remove_all_children/
---

## remove_all_children() {#default}

Removes all the nodes between this range start node and the range end node.


```python
def remove_all_children(self):
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

