---
title: DocumentBuilder.move_to_paragraph method
linktitle: move_to_paragraph method
articleTitle: move_to_paragraph method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_paragraph method. Moves the cursor to a paragraph in the current section."
type: docs
weight: 570
url: /python-net/aspose.words/documentbuilder/move_to_paragraph/
---

## move_to_paragraph(paragraph_index, character_index) {#int_int}

Moves the cursor to a paragraph in the current section.


```python
def move_to_paragraph(self, paragraph_index: int, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| paragraph_index | int |  |
| character_index | int |  |

The navigation is performed inside the current story of the current section.
That is, if you moved the cursor to the primary header of the first section,
then  specified the index of the paragraph inside that header
of that section.

When  is greater than or equal to 0, it specifies an index from
the beginning of the section with 0 being the first paragraph. When is less than 0,
it specified an index from the end of the section with -1 being the last paragraph.




### Examples

Shows how to move a builder's cursor position to a specified paragraph.

```python
doc = aw.Document(MY_DIR + "Paragraphs.docx")
paragraphs = doc.first_section.body.paragraphs

self.assertEqual(22, paragraphs.count)

# Create document builder to edit the document. The builder's cursor,
# which is the point where it will insert new nodes when we call its document construction methods,
# is currently at the beginning of the document.
builder = aw.DocumentBuilder(doc)

self.assertEqual(0, paragraphs.index_of(builder.current_paragraph))

# Move that cursor to a different paragraph will place that cursor in front of that paragraph.
builder.move_to_paragraph(2, 0)

# Any new content that we add will be inserted at that point.
builder.writeln("This is a new third paragraph. ")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

