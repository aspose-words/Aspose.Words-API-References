---
title: DocumentBuilder.move_to_structured_document_tag method
linktitle: move_to_structured_document_tag method
articleTitle: move_to_structured_document_tag method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_structured_document_tag method"
type: docs
weight: 590
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
| structured_document_tag_index | int | The index of the structured document tag to move to. |
| character_index | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

### Remarks

The navigation is performed inside the current story of the current section. That is, if you moved the
cursor to the primary header of the first section, then *structuredDocumentTagIndex*
specified the index of the structured document tag inside that header of that section.

When *structuredDocumentTagIndex* is greater than or equal to 0, it specifies an index
from the beginning of the section with 0 being the first structured document tag. When*structuredDocumentTagIndex* is less than 0, it specified an index from the end of the
section with -1 being the last structured document tag.




## move_to_structured_document_tag(structured_document_tag, character_index) {#structureddocumenttag_int}

Moves the cursor to the structured document tag.


```python
def move_to_structured_document_tag(self, structured_document_tag: aspose.words.markup.StructuredDocumentTag, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| structured_document_tag | [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) | The structured document tag to move to. |
| character_index | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

## Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
builder = aw.DocumentBuilder(doc)
# There is a several ways to move the cursor:
# 1 -  Move to the first character of structured document tag by index.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=1)
# 2 -  Move to the first character of structured document tag by object.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(structured_document_tag=tag, character_index=1)
builder.write(' New text.')
self.assertEqual('R New text.ichText', tag.get_text().strip())
# 3 -  Move to the end of the second structured document tag.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=-1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)
# Get currently selected structured document tag.
builder.current_structured_document_tag.color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Document.MoveToStructuredDocumentTag.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

