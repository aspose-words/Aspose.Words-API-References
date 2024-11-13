---
title: ParagraphFormat.add_space_between_far_east_and_alpha property
linktitle: add_space_between_far_east_and_alpha property
articleTitle: add_space_between_far_east_and_alpha property
second_title: Aspose.Words for Python
description: "ParagraphFormat.add_space_between_far_east_and_alpha property. Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph."
type: docs
weight: 10
url: /python-net/aspose.words/paragraphformat/add_space_between_far_east_and_alpha/
---

## ParagraphFormat.add_space_between_far_east_and_alpha property

Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions
of Latin text and regions of East Asian text in the current paragraph.


```python
@property
def add_space_between_far_east_and_alpha(self) -> bool:
    ...

@add_space_between_far_east_and_alpha.setter
def add_space_between_far_east_and_alpha(self, value: bool):
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

