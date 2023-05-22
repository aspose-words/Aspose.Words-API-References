---
title: DocumentBuilder.move_to_structured_document_tag method
linktitle: move_to_structured_document_tag method
articleTitle: move_to_structured_document_tag method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_structured_document_tag method"
type: docs
weight: 580
url: /python-net/aspose.words/documentbuilder/move_to_structured_document_tag/
---

## move_to_structured_document_tag(structured_document_tag_index, character_index) {#int_int}

Moves the cursor to a structured document tag in the current section.


```python
def move_to_structured_document_tag(self, structured_document_tag_index: int, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| structured_document_tag_index | int |  |
| character_index | int |  |

The navigation is performed inside the current story of the current section. That is, if you moved the
cursor to the primary header of the first section, then 
specified the index of the structured document tag inside that header of that section.

When  is greater than or equal to 0, it specifies an index
from the beginning of the section with 0 being the first structured document tag. When is less than 0, it specified an index from the end of the
section with -1 being the last structured document tag.




## move_to_structured_document_tag(structured_document_tag, character_index) {#structureddocumenttag_int}

Moves the cursor to the structured document tag.


```python
def move_to_structured_document_tag(self, structured_document_tag: aspose.words.markup.StructuredDocumentTag, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| structured_document_tag | [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) |  |
| character_index | int |  |

## Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```python
doc = aw.Document(MY_DIR + "Structured document tags.docx")
builder = aw.DocumentBuilder(doc)

# There is a several ways to move the cursor:
# 1 -  Move to the first character of structured document tag by index.
builder.move_to_structured_document_tag(1, 1)

# 2 -  Move to the first character of structured document tag by object.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(tag, 1)
builder.write(" New text.")

self.assertEqual("R New text.ichText", tag.get_text().strip())

# 3 -  Move to the end of the second structured document tag.
builder.move_to_structured_document_tag(1, -1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)

# Get currently selected structured document tag.
builder.current_structured_document_tag.color = drawing.Color.green

doc.save(ARTIFACTS_DIR + "Document.MoveToStructuredDocumentTag.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

