---
title: CheckBoxControl.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "CheckBoxControl.type property. Gets type of Forms 2.0 control."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/checkboxcontrol/type/
---

## CheckBoxControl.type property

Gets type of Forms 2.0 control.


```python
@property
def type(self) -> aspose.words.drawing.ole.Forms2OleControlType:
    ...

```

### Examples

Shows how to change state of the CheckBox control.

```python
doc = aw.Document(file_name=MY_DIR + 'ActiveX controls.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
check_box_control = shape.ole_format.ole_control.as_check_box_control()
check_box_control.checked = True
self.assertEqual(True, check_box_control.checked)
self.assertEqual(aw.drawing.ole.Forms2OleControlType.CHECK_BOX, check_box_control.type)
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [CheckBoxControl](../)

