---
title: Table.vertical_anchor property
linktitle: vertical_anchor property
articleTitle: vertical_anchor property
second_title: Aspose.Words for Python
description: "Table.vertical_anchor property. Gets the base object from which the vertical positioning of floating table should be calculated"
type: docs
weight: 340
url: /zh/python-net/aspose.words.tables/table/vertical_anchor/
---

## Table.vertical_anchor property

Gets the base object from which the vertical positioning of floating table should be calculated.
Default value is [RelativeVerticalPosition.MARGIN](../../../aspose.words.drawing/relativeverticalposition/#MARGIN).



```python
@property
def vertical_anchor(self) -> aspose.words.drawing.RelativeVerticalPosition:
    ...

@vertical_anchor.setter
def vertical_anchor(self, value: aspose.words.drawing.RelativeVerticalPosition):
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
    # RelativeHorizontalPosition 中仅在 HorizontalAnchor 设置器中提供 Margin、Page、Column。
    # 对于任何其他值将抛出 ArgumentException。
    table.horizontal_anchor = aw.drawing.RelativeHorizontalPosition.COLUMN
    # RelativeVerticalPosition 中仅在 VerticalAnchor 设置器中提供 Margin、Page、Paragraph。
    # 对于任何其他值将抛出 ArgumentException。
    table.vertical_anchor = aw.drawing.RelativeVerticalPosition.PAGE
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

