---
title: OleControl.is_forms2_ole_control property
linktitle: is_forms2_ole_control property
articleTitle: is_forms2_ole_control property
second_title: Aspose.Words for Python
description: "OleControl.is_forms2_ole_control property. Returns ``True`` if the control is a [Forms2OleControl](../../forms2olecontrol/)."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/olecontrol/is_forms2_ole_control/
---

## OleControl.is_forms2_ole_control property

Returns ``True`` if the control is a [Forms2OleControl](../../forms2olecontrol/).



```python
@property
def is_forms2_ole_control(self) -> bool:
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
* class [OleControl](../)

