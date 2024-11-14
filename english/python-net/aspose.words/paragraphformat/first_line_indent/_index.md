---
title: ParagraphFormat.first_line_indent property
linktitle: first_line_indent property
articleTitle: first_line_indent property
second_title: Aspose.Words for Python
description: "ParagraphFormat.first_line_indent property. Gets or sets the value (in points) for a first line or hanging indent"
type: docs
weight: 120
url: /python-net/aspose.words/paragraphformat/first_line_indent/
---

## ParagraphFormat.first_line_indent property

Gets or sets the value (in points) for a first line or hanging indent.
Use positive values to set the first-line indent, and negative values to set the hanging indent.




```python
@property
def first_line_indent(self) -> float:
    ...

@first_line_indent.setter
def first_line_indent(self, value: float):
    ...

```

### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Arial'
font.underline = aw.Underline.DASH
paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True
# The "Writeln" method ends the paragraph after appending text
# and then starts a new line, adding a new paragraph.
builder.writeln('Hello world!')
self.assertTrue(builder.current_paragraph.is_end_of_document)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

