---
title: ParagraphFormat.add_space_between_far_east_and_digit property
linktitle: add_space_between_far_east_and_digit property
articleTitle: add_space_between_far_east_and_digit property
second_title: Aspose.Words for Python
description: "ParagraphFormat.add_space_between_far_east_and_digit property. Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph."
type: docs
weight: 20
url: /python-net/aspose.words/paragraphformat/add_space_between_far_east_and_digit/
---

## ParagraphFormat.add_space_between_far_east_and_digit property

Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions
of numbers and regions of East Asian text in the current paragraph.


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
* class [ParagraphFormat](../)

