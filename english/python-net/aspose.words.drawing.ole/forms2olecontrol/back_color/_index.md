---
title: Forms2OleControl.back_color property
linktitle: back_color property
articleTitle: back_color property
second_title: Aspose.Words for Python
description: "Forms2OleControl.back_color property. Gets or sets a background color of the control"
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/back_color/
---

## Forms2OleControl.back_color property

Gets or sets a background color of the control.
The default value depends on a type of the control.


```python
@property
def back_color(self) -> aspose.pydrawing.Color:
    ...

@back_color.setter
def back_color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to set properties for ActiveX control.

```python
doc = aw.Document(file_name=MY_DIR + 'ActiveX controls.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
ole_control = shape.ole_format.ole_control.as_forms2_ole_control()
ole_control.fore_color = aspose.pydrawing.Color.from_argb(23, 225, 53)
ole_control.back_color = aspose.pydrawing.Color.from_argb(51, 151, 244)
ole_control.height = 100.54
ole_control.width = 201.06
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [Forms2OleControl](../)

