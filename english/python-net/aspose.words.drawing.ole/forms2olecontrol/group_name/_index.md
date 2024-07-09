---
title: Forms2OleControl.group_name property
linktitle: group_name property
articleTitle: group_name property
second_title: Aspose.Words for Python
description: "Forms2OleControl.group_name property. Gets or sets a string that specifies a group of mutually exclusive controls"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/group_name/
---

## Forms2OleControl.group_name property

Gets or sets a string that specifies a group of mutually exclusive controls.
The default value is an empty string.


```python
@property
def group_name(self) -> str:
    ...

@group_name.setter
def group_name(self, value: str):
    ...

```

### Examples

Shows how to verify the properties of an ActiveX control.

```python
doc = aw.Document(file_name=MY_DIR + 'ActiveX controls.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
ole_control = shape.ole_format.ole_control
self.assertEqual('CheckBox1', ole_control.name)
if ole_control.is_forms2_ole_control:
    check_box = ole_control.as_forms2_ole_control()
    self.assertEqual('First', check_box.caption)
    self.assertEqual('0', check_box.value)
    self.assertEqual(True, check_box.enabled)
    self.assertEqual(aw.drawing.ole.Forms2OleControlType.CHECK_BOX, check_box.type)
    self.assertEqual(None, check_box.child_nodes)
    self.assertEqual('', check_box.group_name)
    # Note, that you can't set GroupName for a Frame.
    check_box.group_name = 'Aspose group name'
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [Forms2OleControl](../)

