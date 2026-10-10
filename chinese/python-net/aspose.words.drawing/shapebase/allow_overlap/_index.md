---
title: ShapeBase.allow_overlap property
linktitle: allow_overlap property
articleTitle: allow_overlap property
second_title: Aspose.Words for Python
description: "ShapeBase.allow_overlap property. Gets or sets a value that specifies whether this shape can overlap other shapes."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing/shapebase/allow_overlap/
---

## ShapeBase.allow_overlap property

Gets or sets a value that specifies whether this shape can overlap other shapes.


```python
@property
def allow_overlap(self) -> bool:
    ...

@allow_overlap.setter
def allow_overlap(self, value: bool):
    ...

```

### Remarks

This property affects behavior of the shape in Microsoft Word.
Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is ``True``.




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

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

