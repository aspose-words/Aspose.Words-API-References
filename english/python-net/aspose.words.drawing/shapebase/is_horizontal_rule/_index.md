---
title: ShapeBase.is_horizontal_rule property
linktitle: is_horizontal_rule property
articleTitle: is_horizontal_rule property
second_title: Aspose.Words for Python
description: "ShapeBase.is_horizontal_rule property. Returns ``True`` if this shape is a horizontal rule."
type: docs
weight: 290
url: /python-net/aspose.words.drawing/shapebase/is_horizontal_rule/
---

## ShapeBase.is_horizontal_rule property

Returns ``True`` if this shape is a horizontal rule.



```python
@property
def is_horizontal_rule(self) -> bool:
    ...

```

### Examples

Shows how to insert a horizontal rule shape, and customize its formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_horizontal_rule()
horizontal_rule_format = shape.horizontal_rule_format
horizontal_rule_format.alignment = aw.drawing.HorizontalRuleAlignment.CENTER
horizontal_rule_format.width_percent = 70
horizontal_rule_format.height = 3
horizontal_rule_format.color = aspose.pydrawing.Color.blue
horizontal_rule_format.no_shade = True
self.assertTrue(shape.is_horizontal_rule)
self.assertTrue(shape.horizontal_rule_format.no_shade)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

