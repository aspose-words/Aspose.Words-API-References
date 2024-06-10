---
title: Story.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "Story.first_paragraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /python-net/aspose.words/story/first_paragraph/
---

## Story.first_paragraph property

Gets the first paragraph in the story.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

Shows how to create and format a text box.

```python
doc = aw.Document()
# Create a floating text box.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# Set the horizontal, and vertical alignment of the text inside the shape.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# Add a paragraph to the text box and add a run of text that the text box will display.
text_box.append_child(aw.Paragraph(doc))
para = text_box.first_paragraph
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
run = aw.Run(doc)
run.text = 'Hello world!'
para.append_child(run)
doc.first_section.body.first_paragraph.append_child(text_box)
doc.save(ARTIFACTS_DIR + 'Shape.create_text_box.docx')
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

