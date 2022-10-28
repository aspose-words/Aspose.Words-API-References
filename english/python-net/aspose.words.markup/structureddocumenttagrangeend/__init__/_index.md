---
title: StructuredDocumentTagRangeEnd constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "Initializes a new instance of the Structured document tag range end class."
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
| doc | [DocumentBase](../../../aspose.words/documentbase/) |  |
| id | int |  |

### Examples

Shows how to create/remove structured document tag and its content.

```python
def test_sdt_range_extended_methods(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.writeln("StructuredDocumentTag element")

    range_start = self.insert_structured_document_tag_ranges(doc)

    # Removes ranged structured document tag, but keeps content inside.
    range_start.remove_self_only()

    range_start = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, False)
    self.assertIsNone(range_start)

    range_end = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, False)
    self.assertIsNone(range_end)

    self.assertEqual("StructuredDocumentTag element", doc.get_text().strip())

    range_start = self.insert_structured_document_tag_ranges(doc)

    paragraph_node = range_start.last_child
    self.assertEqual("StructuredDocumentTag element", paragraph_node.get_text().strip())

    # Removes ranged structured document tag and content inside.
    range_start.remove_all_children()

    self.assertEquals(0, range_start.child_nodes.count)

def insert_structured_document_tag_ranges(self, doc: aw.Document) -> aw.markup.StructuredDocumentTagRangeStart:

    range_start = aw.markup.StructuredDocumentTagRangeStart(doc, aw.markup.SdtType.PLAIN_TEXT)
    range_end = aw.markup.StructuredDocumentTagRangeEnd(doc, range_start.id)

    doc.first_section.body.insert_before(range_start, doc.first_section.body.first_paragraph)
    doc.last_section.body.insert_after(range_end, doc.first_section.body.first_paragraph)
    return range_start
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeEnd](../)

