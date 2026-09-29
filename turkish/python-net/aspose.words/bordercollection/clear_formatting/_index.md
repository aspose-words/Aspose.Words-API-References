---
title: BorderCollection.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "BorderCollection.clear_formatting method. Removes all borders of an object."
type: docs
weight: 140
url: /tr/python-net/aspose.words/bordercollection/clear_formatting/
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
doc = aw.Document(file_name=MY_DIR + 'Borders.docx')
# Bu belgenin ilk paragrafı, bu ayarlarla görünür kenarlıklara sahiptir.
first_paragraph_borders = doc.first_section.body.first_paragraph.paragraph_format.borders
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), first_paragraph_borders.color.to_argb())
self.assertEqual(aw.LineStyle.SINGLE, first_paragraph_borders.line_style)
self.assertEqual(3, first_paragraph_borders.line_width)
# Tüm kenarlıkları kaldırmak için her paragrafta "ClearFormatting" metodunu kullanın.
for paragraph in doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    paragraph.paragraph_format.borders.clear_formatting()
    for border in paragraph.paragraph_format.borders:
        self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
        self.assertEqual(aw.LineStyle.NONE, border.line_style)
        self.assertEqual(0, border.line_width)
doc.save(file_name=ARTIFACTS_DIR + 'BorderCollection.RemoveAllBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

