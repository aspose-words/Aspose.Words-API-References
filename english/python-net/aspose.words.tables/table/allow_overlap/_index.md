---
title: Table.allow_overlap property
linktitle: allow_overlap property
articleTitle: allow_overlap property
second_title: Aspose.Words for Python
description: "Table.allow_overlap property. Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed"
type: docs
weight: 70
url: /python-net/aspose.words.tables/table/allow_overlap/
---

## Table.allow_overlap property

Gets whether a floating table shall allow other floating objects in the document
to overlap its extents when displayed.
Default value is ``True``.



```python
@property
def allow_overlap(self) -> bool:
    ...

```

### Examples

Shows how to work with floating tables properties.

```python
doc = aw.Document(MY_DIR + "Table wrapped by text.docx")

table = doc.first_section.body.tables[0]

if table.text_wrapping == aw.tables.TextWrapping.AROUND:
    self.assertEqual(aw.drawing.RelativeHorizontalPosition.MARGIN, table.horizontal_anchor)
    self.assertEqual(aw.drawing.RelativeVerticalPosition.PARAGRAPH, table.vertical_anchor)
    self.assertEqual(False, table.allow_overlap)

    # Only MARGIN, PAGE, COLUMN available in RelativeHorizontalPosition for horizontal_anchor setter.
    # The Exception will be thrown for any other values.
    table.horizontal_anchor = aw.drawing.RelativeHorizontalPosition.COLUMN

    # Only MARGIN, PAGE, PARAGRAPH available in RelativeVerticalPosition for vertical_anchor setter.
    # The Exception will be thrown for any other values.
    table.vertical_anchor = aw.drawing.RelativeVerticalPosition.PAGE
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

