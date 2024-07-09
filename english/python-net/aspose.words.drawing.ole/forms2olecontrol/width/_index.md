---
title: Forms2OleControl.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "Forms2OleControl.width property. Gets or sets a width of the control in points."
type: docs
weight: 100
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/width/
---

## Forms2OleControl.width property

Gets or sets a width of the control in points.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
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

