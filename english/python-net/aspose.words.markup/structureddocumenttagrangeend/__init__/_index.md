---
title: StructuredDocumentTagRangeEnd constructor
linktitle: StructuredDocumentTagRangeEnd constructor
articleTitle: StructuredDocumentTagRangeEnd constructor
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeEnd constructor. Initializes a new instance of the Structured document tag range end class."
type: docs
weight: 10
url: /python-net/aspose.words.markup/structureddocumenttagrangeend/__init__/
---

## StructuredDocumentTagRangeEnd(doc, id) {#documentbase_int}

Initializes a new instance of the **Structured document tag range end** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, id: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| id | int | Identifier of the corresponding structured document tag range start. |

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
* class [StructuredDocumentTagRangeEnd](../)

