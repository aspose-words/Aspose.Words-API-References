---
title: CheckBoxControl.checked property
linktitle: checked property
articleTitle: checked property
second_title: Aspose.Words for Python
description: "CheckBoxControl.checked property. Gets or sets a boolean value indicating either this [CheckBoxControl](../) is checked or not"
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/checkboxcontrol/checked/
---

## CheckBoxControl.checked property

Gets or sets a boolean value indicating either this [CheckBoxControl](../) is checked or not.
The default value is ``False``.



```python
@property
def checked(self) -> bool:
    ...

@checked.setter
def checked(self, value: bool):
    ...

```

### Examples

Shows how to change state of the CheckBox control.

```python
doc = aw.Document(file_name=MY_DIR + 'ActiveX controls.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
check_box_control = shape.ole_format.ole_control.as_check_box_control()
check_box_control.checked = True
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [CheckBoxControl](../)

