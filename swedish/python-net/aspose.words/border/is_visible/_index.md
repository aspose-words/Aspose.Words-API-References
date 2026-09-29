---
title: Border.is_visible property
linktitle: is_visible property
articleTitle: is_visible property
second_title: Aspose.Words for Python
description: "Border.is_visible property. Returns ``True`` if the [Border.line_style](../line_style/) is not [LineStyle.NONE](../../linestyle/#NONE)."
type: docs
weight: 30
url: /sv/python-net/aspose.words/border/is_visible/
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
# Varje stycke har en individuell uppsättning av kanter.
# Vi kan komma åt inställningarna för utseendet på dessa kanter via paragraph format-objektet.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), borders[0].color.to_argb())
self.assertEqual(3, borders[0].line_width)
self.assertEqual(aw.LineStyle.SINGLE, borders[0].line_style)
self.assertTrue(borders[0].is_visible)
# Vi kan ta bort en kant på en gång genom att köra ClearFormatting-metoden.
# Att köra den här metoden på varje kant i ett stycke kommer att ta bort alla dess kanter.
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

