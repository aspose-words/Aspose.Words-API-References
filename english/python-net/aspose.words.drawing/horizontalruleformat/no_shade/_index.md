---
title: no_shade property
second_title: Aspose.Words for Python via .NET API Reference
description: "Indicates the presence of 3D shading for the horizontal rule"
type: docs
weight: 40
url: /python-net/aspose.words.drawing/horizontalruleformat/no_shade/
---

## HorizontalRuleFormat.no_shade property

Indicates the presence of 3D shading for the horizontal rule.
If true, then the horizontal rule is without 3D shading and solid color is used.

The default value is false.




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
horizontal_rule_format.color = drawing.Color.blue
horizontal_rule_format.no_shade = True

self.assertTrue(shape.is_horizontal_rule)
self.assertTrue(shape.horizontal_rule_format.no_shade)
```

### See Also

* module [aspose.words.drawing](../../)
* class [HorizontalRuleFormat](../)

