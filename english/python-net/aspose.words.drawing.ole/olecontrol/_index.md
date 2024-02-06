---
title: OleControl class
linktitle: OleControl class
articleTitle: OleControl class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ole.OleControl class. Represents OLE ActiveX control"
type: docs
weight: 50
url: /python-net/aspose.words.drawing.ole/olecontrol/
---

## OleControl class

Represents OLE ActiveX control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/python-net/working-with-ole-objects/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [is_forms2_ole_control](./is_forms2_ole_control/) | Returns ``True`` if the control is a [Forms2OleControl](../forms2olecontrol/). |
| [name](./name/) | Gets or sets name of the ActiveX control. |

### Methods

| Name | Description |
| --- | --- |
|[ as_forms2_ole_control()](./as_forms2_ole_control/#default) |  |

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

* module [aspose.words.drawing.ole](../)

