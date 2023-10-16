---
title: DocumentBuilder.insert_paragraph method
linktitle: insert_paragraph method
articleTitle: insert_paragraph method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_paragraph method. Inserts a paragraph break into the document."
type: docs
weight: 430
url: /python-net/aspose.words/documentbuilder/insert_paragraph/
---

## insert_paragraph() {#default}

Inserts a paragraph break into the document.


```python
def insert_paragraph(self):
    ...
```

Current paragraph formatting specified by the [DocumentBuilder.paragraph_format](../paragraph_format/) property is used.

Breaks the current paragraph in two. After inserting the paragraph, the cursor is placed at the beginning of the new paragraph.

An exception is thrown if it is not possible to insert a paragraph break at the current cursor position.




### Returns

The paragraph node that was just inserted. It is the same node as [DocumentBuilder.current_paragraph](../current_paragraph/).


### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

font = builder.font
font.size = 16
font.bold = True
font.color = drawing.Color.blue
font.name = "Arial"
font.underline = aw.Underline.DASH

paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True

# The "writeln" method ends the paragraph after appending text
# and then starts a new line, adding a new paragraph.
builder.writeln("Hello world!")

self.assertTrue(builder.current_paragraph.is_end_of_document)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

