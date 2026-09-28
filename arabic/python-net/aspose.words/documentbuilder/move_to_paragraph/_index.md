---
title: DocumentBuilder.move_to_paragraph method
linktitle: move_to_paragraph method
articleTitle: move_to_paragraph method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_paragraph method. Moves the cursor to a paragraph in the current section."
type: docs
weight: 600
url: /ar/python-net/aspose.words/documentbuilder/move_to_paragraph/
---

## move_to_paragraph(paragraph_index, character_index) {#int_int}

Moves the cursor to a paragraph in the current section.


```python
def move_to_paragraph(self, paragraph_index: int, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| paragraph_index | int | The index of the paragraph to move to. |
| character_index | int | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |

### Remarks

The navigation is performed inside the current story of the current section.
That is, if you moved the cursor to the primary header of the first section,
then *paragraphIndex* specified the index of the paragraph inside that header
of that section.

When *paragraphIndex* is greater than or equal to 0, it specifies an index from
the beginning of the section with 0 being the first paragraph. When*paragraphIndex* is less than 0,
it specified an index from the end of the section with -1 being the last paragraph.




### Examples

Shows how to move a builder's cursor position to a specified paragraph.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(22, paragraphs.count)
# أنشئ باني المستند لتحرير المستند. مؤشر الباني،
# وهو النقطة التي سيُدرج عندها عقد جديدة عندما نستدعي طرق بناء المستند الخاصة به،
# حاليًا في بداية المستند.
builder = aw.DocumentBuilder(doc=doc)
self.assertEqual(0, paragraphs.index_of(builder.current_paragraph))
# نقل ذلك المؤشر إلى فقرة مختلفة سيضع المؤشر أمام تلك الفقرة.
builder.move_to_paragraph(2, 0)
# أي محتوى جديد نضيفه سيُدرج في تلك النقطة.
builder.writeln('This is a new third paragraph. ')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

