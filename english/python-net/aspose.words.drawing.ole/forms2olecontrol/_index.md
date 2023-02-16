---
title: Forms2OleControl class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents Microsoft Forms 2.0 OLE control"
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/forms2olecontrol/
---

## Forms2OleControl class

Represents Microsoft Forms 2.0 OLE control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/python-net/working-with-ole-objects/) documentation article.




**Inheritance:** [Forms2OleControl](./) → [OleControl](../olecontrol/)

### Properties

| Name | Description |
| --- | --- |
| [caption](./caption/) | Gets Caption property of control. Default value is an empty string. |
| [child_nodes](./child_nodes/) | Gets collection of immediate child controls. |
| [enabled](./enabled/) | Returns ``True`` if control is in enabled state. |
| [is_forms2_ole_control](../olecontrol/is_forms2_ole_control/) | Returns ``True`` if the control is a [Forms2OleControl](./).<br>(Inherited from [OleControl](../olecontrol/)) |
| [name](../olecontrol/name/) | Gets name of the ActiveX control.<br>(Inherited from [OleControl](../olecontrol/)) |
| [type](./type/) | Gets type of Forms 2.0 control. |
| [value](./value/) | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |

### Methods

| Name | Description |
| --- | --- |

### Examples

Shows how to verify the properties of an ActiveX control.

```python
doc = aw.Document(MY_DIR + "ActiveX controls.docx")

shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
ole_control = shape.ole_format.ole_control

self.assertEqual("CheckBox1", ole_control.name);

if ole_control.is_forms2_ole_control:

    check_box = ole_control.as_forms2_ole_control()
    self.assertEqual("Первый", check_box.caption)
    self.assertEqual("0", check_box.value)
    self.assertEqual(True, check_box.enabled)
    self.assertEqual(aw.drawing.ole.Forms2OleControlType.CHECK_BOX, check_box.type)
    self.assertIsNone(check_box.child_nodes)
```

### See Also

* module [aspose.words.drawing.ole](../)
* class [OleControl](../olecontrol/)

