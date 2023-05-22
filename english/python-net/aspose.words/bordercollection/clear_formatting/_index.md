---
title: BorderCollection.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "BorderCollection.clear_formatting method. Removes all borders of an object."
type: docs
weight: 140
url: /python-net/aspose.words/bordercollection/clear_formatting/
---

## clear_formatting() {#default}

Removes all borders of an object.


```python
def clear_formatting(self):
    ...
```

### Examples

Shows how to remove all borders from all paragraphs in a document.

```python
doc = aw.Document(MY_DIR + "Borders.docx")

# The first paragraph of this document has visible borders with these settings.
first_paragraph_borders = doc.first_section.body.first_paragraph.paragraph_format.borders

self.assertEqual(drawing.Color.red.to_argb(), first_paragraph_borders.color.to_argb())
self.assertEqual(aw.LineStyle.SINGLE, first_paragraph_borders.line_style)
self.assertEqual(3.0, first_paragraph_borders.line_width)

# Use the "clear_formatting" method on each paragraph to remove all borders.
for paragraph in doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    paragraph.paragraph_format.borders.clear_formatting()

    for border in paragraph.paragraph_format.borders:
        self.assertEqual(drawing.Color.empty().to_argb(), border.color.to_argb())
        self.assertEqual(aw.LineStyle.NONE, border.line_style)
        self.assertEqual(0.0, border.line_width)

doc.save(ARTIFACTS_DIR + "BorderCollection.remove_all_borders.docx")
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

