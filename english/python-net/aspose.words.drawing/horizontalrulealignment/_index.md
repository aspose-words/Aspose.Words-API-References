---
title: HorizontalRuleAlignment enumeration
linktitle: HorizontalRuleAlignment enumeration
articleTitle: HorizontalRuleAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.HorizontalRuleAlignment enumeration. Represents the alignment for the specified horizontal rule."
type: docs
weight: 180
url: /python-net/aspose.words.drawing/horizontalrulealignment/
---

## HorizontalRuleAlignment enumeration

Represents the alignment for the specified horizontal rule.


### Members

| Name | Description |
| --- | --- |
| LEFT | Aligned to the left. |
| CENTER | Aligned to the center. |
| RIGHT | Aligned to the right. |

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

* module [aspose.words.drawing](../)

