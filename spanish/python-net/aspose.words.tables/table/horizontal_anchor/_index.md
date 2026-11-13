---
title: Table.horizontal_anchor property
linktitle: horizontal_anchor property
articleTitle: horizontal_anchor property
second_title: Aspose.Words for Python
description: "Table.horizontal_anchor property. Gets the base object from which the horizontal positioning of floating table should be calculated"
type: docs
weight: 170
url: /es/python-net/aspose.words.tables/table/horizontal_anchor/
---

## Table.horizontal_anchor property

Gets the base object from which the horizontal positioning of floating table should be calculated.
Default value is [RelativeHorizontalPosition.COLUMN](../../../aspose.words.drawing/relativehorizontalposition/#COLUMN).



```python
@property
def horizontal_anchor(self) -> aspose.words.drawing.RelativeHorizontalPosition:
    ...

@horizontal_anchor.setter
def horizontal_anchor(self, value: aspose.words.drawing.RelativeHorizontalPosition):
    ...

```

### Examples

Shows how to work with floating tables properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Table wrapped by text.docx')
table = doc.first_section.body.tables[0]
if table.text_wrapping == aw.tables.TextWrapping.AROUND:
    self.assertEqual(aw.drawing.RelativeHorizontalPosition.MARGIN, table.horizontal_anchor)
    self.assertEqual(aw.drawing.RelativeVerticalPosition.PARAGRAPH, table.vertical_anchor)
    self.assertEqual(False, table.allow_overlap)
    # Solo Margin, Page, Column están disponibles en RelativeHorizontalPosition para el setter HorizontalAnchor.
    # Se lanzará una ArgumentException para cualquier otro valor.
    table.horizontal_anchor = aw.drawing.RelativeHorizontalPosition.COLUMN
    # Solo Margin, Page, Paragraph están disponibles en RelativeVerticalPosition para el setter VerticalAnchor.
    # Se lanzará una ArgumentException para cualquier otro valor.
    table.vertical_anchor = aw.drawing.RelativeVerticalPosition.PAGE
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

