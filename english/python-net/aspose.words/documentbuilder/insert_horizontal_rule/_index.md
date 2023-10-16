---
title: DocumentBuilder.insert_horizontal_rule method
linktitle: insert_horizontal_rule method
articleTitle: insert_horizontal_rule method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_horizontal_rule method. Inserts a horizontal rule shape into the document."
type: docs
weight: 350
url: /python-net/aspose.words/documentbuilder/insert_horizontal_rule/
---

## insert_horizontal_rule() {#default}

Inserts a horizontal rule shape into the document.


```python
def insert_horizontal_rule(self):
    ...
```

### Returns

The shape that is a horizontal rule.


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

* module [aspose.words](../../)
* class [DocumentBuilder](../)

