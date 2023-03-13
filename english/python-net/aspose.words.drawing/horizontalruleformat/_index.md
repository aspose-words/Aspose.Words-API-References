﻿---
title: HorizontalRuleFormat class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents horizontal rule formatting"
type: docs
weight: 160
url: /python-net/aspose.words.drawing/horizontalruleformat/
---

## HorizontalRuleFormat class

Represents horizontal rule formatting.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the alignment of the horizontal rule. |
| [color](./color/) | Gets or sets the brush color that fills the horizontal rule. |
| [height](./height/) | Gets or sets the height of the horizontal rule. |
| [no_shade](./no_shade/) | Indicates the presence of 3D shading for the horizontal rule. If ``True``, then the horizontal rule is without 3D shading and solid color is used. |
| [width_percent](./width_percent/) | Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width. |

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

* module [aspose.words.drawing](../)

