---
title: HorizontalRuleFormat.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "HorizontalRuleFormat.height property. Gets or sets the height of the horizontal rule."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/horizontalruleformat/height/
---

## HorizontalRuleFormat.height property

Gets or sets the height of the horizontal rule.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

This is a shortcut to the [ShapeBase.height](../../shapebase/height/) property.

Valid values ​​range from 0 to 1584 inclusive.

The default value is 1.5.




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
* class [HorizontalRuleFormat](../)

