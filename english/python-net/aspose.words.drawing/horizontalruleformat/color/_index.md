---
title: HorizontalRuleFormat.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "HorizontalRuleFormat.color property. Gets or sets the brush color that fills the horizontal rule."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/horizontalruleformat/color/
---

## HorizontalRuleFormat.color property

Gets or sets the brush color that fills the horizontal rule.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.gray.





### Examples

Shows how to insert a horizontal rule shape, and customize its formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
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

