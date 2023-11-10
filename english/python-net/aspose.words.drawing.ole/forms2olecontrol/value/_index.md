---
title: Forms2OleControl.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "Forms2OleControl.value property. Gets underlying Value property which often represents control state"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/value/
---

## Forms2OleControl.value property

Gets underlying Value property which often represents control state.
For example checked option button has '1' value while unchecked has '0'.
Default value is an empty string.


```python
@property
def value(self) -> str:
    ...

```

### Examples

Shows how to verify the properties of an ActiveX control.

```python
doc = aw.Document(MY_DIR + "ActiveX controls.docx")

shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
ole_control = shape.ole_format.ole_control

self.assertEqual("CheckBox1", ole_control.name)

if ole_control.is_forms2_ole_control:

    check_box = ole_control.as_forms2_ole_control()
    self.assertEqual("Первый", check_box.caption)
    self.assertEqual("0", check_box.value)
    self.assertEqual(True, check_box.enabled)
    self.assertEqual(aw.drawing.ole.Forms2OleControlType.CHECK_BOX, check_box.type)
    self.assertIsNone(check_box.child_nodes)
    self.assertEqual("", check_box.group_name)

    # Note, that you can't set GroupName for a Frame.
    check_box.group_name = "Aspose group name"
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [Forms2OleControl](../)

