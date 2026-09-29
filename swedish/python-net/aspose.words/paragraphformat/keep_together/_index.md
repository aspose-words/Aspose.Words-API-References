---
title: ParagraphFormat.keep_together property
linktitle: keep_together property
articleTitle: keep_together property
second_title: Aspose.Words for Python
description: "ParagraphFormat.keep_together property. True if all lines in the paragraph are to remain on the same page."
type: docs
weight: 160
url: /sv/python-net/aspose.words/paragraphformat/keep_together/
---

## ParagraphFormat.keep_together property

True if all lines in the paragraph are to remain on the same page.


```python
@property
def keep_together(self) -> bool:
    ...

@keep_together.setter
def keep_together(self, value: bool):
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
# Metoden \"Writeln\" avslutar stycket efter att ha lagt till text
# och startar sedan en ny rad, vilket lägger till ett nytt stycke.
builder.writeln('Hello world!')
self.assertTrue(builder.current_paragraph.is_end_of_document)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

