---
title: Border.is_visible property
linktitle: is_visible property
articleTitle: is_visible property
second_title: Aspose.Words for Python
description: "Border.is_visible property. Returns ``True`` if the [Border.line_style](../line_style/) is not [LineStyle.NONE](../../linestyle/#NONE)."
type: docs
weight: 30
url: /python-net/aspose.words/border/is_visible/
---

## Border.is_visible property

Returns ``True`` if the [Border.line_style](../line_style/) is not [LineStyle.NONE](../../linestyle/#NONE).



```python
@property
def is_visible(self) -> bool:
    ...

```

### Examples

Shows how to remove borders from a paragraph.

```python
doc = aw.Document(file_name=MY_DIR + 'Borders.docx')
# Each paragraph has an individual set of borders.
# We can access the settings for the appearance of these borders via the paragraph format object.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), borders[0].color.to_argb())
self.assertEqual(3, borders[0].line_width)
self.assertEqual(aw.LineStyle.SINGLE, borders[0].line_style)
self.assertTrue(borders[0].is_visible)
# We can remove a border at once by running the ClearFormatting method.
# Running this method on every border of a paragraph will remove all its borders.
for border in borders:
    border.clear_formatting()
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), borders[0].color.to_argb())
self.assertEqual(0, borders[0].line_width)
self.assertEqual(aw.LineStyle.NONE, borders[0].line_style)
self.assertFalse(borders[0].is_visible)
doc.save(file_name=ARTIFACTS_DIR + 'Border.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

