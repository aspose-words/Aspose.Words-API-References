---
title: vertical_anchor property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the base object from which the vertical positioning of floating table should be calculated"
type: docs
weight: 340
url: /python-net/aspose.words.tables/table/vertical_anchor/
---

## Table.vertical_anchor property

Gets the base object from which the vertical positioning of floating table should be calculated.
Default value is [RelativeVerticalPosition.MARGIN](../../../aspose.words.drawing/relativeverticalposition/#MARGIN).



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

