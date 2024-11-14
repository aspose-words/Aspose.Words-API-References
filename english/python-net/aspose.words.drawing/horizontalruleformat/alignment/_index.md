---
title: HorizontalRuleFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "HorizontalRuleFormat.alignment property. Gets or sets the alignment of the horizontal rule."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/horizontalruleformat/alignment/
---

## HorizontalRuleFormat.alignment property

Gets or sets the alignment of the horizontal rule.


```python
@property
def alignment(self) -> aspose.words.drawing.HorizontalRuleAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.drawing.HorizontalRuleAlignment):
    ...

```

### Remarks

The default value is [HorizontalRuleAlignment.LEFT](../../horizontalrulealignment/#LEFT).




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

