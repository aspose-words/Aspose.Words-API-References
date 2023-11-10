---
title: HorizontalRuleFormat.width_percent property
linktitle: width_percent property
articleTitle: width_percent property
second_title: Aspose.Words for Python
description: "HorizontalRuleFormat.width_percent property. Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width."
type: docs
weight: 50
url: /python-net/aspose.words.drawing/horizontalruleformat/width_percent/
---

## HorizontalRuleFormat.width_percent property

Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width.


```python
@property
def width_percent(self) -> float:
    ...

@width_percent.setter
def width_percent(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Valid values ​​range from 1 to 100 inclusive.

The default value is 100.




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

