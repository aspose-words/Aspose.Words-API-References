---
title: Forms2OleControl.child_nodes property
linktitle: child_nodes property
articleTitle: child_nodes property
second_title: Aspose.Words for Python
description: "Forms2OleControl.child_nodes property. Gets collection of immediate child controls."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/child_nodes/
---

## Forms2OleControl.child_nodes property

Gets collection of immediate child controls.


```python
@property
def child_nodes(self) -> aspose.words.drawing.ole.Forms2OleControlCollection:
    ...

```

### Remarks

Returns ``None`` if this control can not have children.


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

