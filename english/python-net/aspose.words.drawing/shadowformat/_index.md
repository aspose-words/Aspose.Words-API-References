---
title: ShadowFormat class
linktitle: ShadowFormat class
articleTitle: ShadowFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShadowFormat class. Represents shadow formatting for an object"
type: docs
weight: 340
url: /python-net/aspose.words.drawing/shadowformat/
---

## ShadowFormat class

Represents shadow formatting for an object.
To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets a aspose.pydrawing.Color object that represents the color for the shadow. The default value is aspose.pydrawing.Color.black. |
| [transparency](./transparency/) | Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0. |
| [type](./type/) | Gets or sets the specified [ShadowType](../shadowtype/) for ShadowFormat. |
| [visible](./visible/) | Returns ``True`` if the formatting applied to this instance is visible. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Clears shadow format. |

### Examples

Shows how to get shadow color.

```python
doc = aw.Document(file_name=MY_DIR + 'Shadow color.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shadow_format = shape.shadow_format
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shadow_format.color.to_argb())
self.assertEqual(aw.drawing.ShadowType.SHADOW_MIXED, shadow_format.type)
```

### See Also

* module [aspose.words.drawing](../)

