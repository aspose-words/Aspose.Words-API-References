---
title: Border.is_visible property
linktitle: is_visible property
articleTitle: is_visible property
second_title: Aspose.Words for Python
description: "Border.is_visible property. Returns ``True`` if the [Border.line_style](../line_style/) is not [LineStyle.NONE](../../linestyle/#NONE)."
type: docs
weight: 30
url: /it/python-net/aspose.words/border/is_visible/
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
# Ogni paragrafo ha un set individuale di bordi.
# Possiamo accedere alle impostazioni per l'aspetto di questi bordi tramite l'oggetto di formato del paragrafo.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), borders[0].color.to_argb())
self.assertEqual(3, borders[0].line_width)
self.assertEqual(aw.LineStyle.SINGLE, borders[0].line_style)
self.assertTrue(borders[0].is_visible)
# Possiamo rimuovere un bordo in una volta eseguendo il metodo ClearFormatting.
# Eseguire questo metodo su ogni bordo di un paragrafo rimuoverà tutti i suoi bordi.
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

