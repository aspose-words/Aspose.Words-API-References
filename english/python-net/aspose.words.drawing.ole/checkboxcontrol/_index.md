---
title: CheckBoxControl class
linktitle: CheckBoxControl class
articleTitle: CheckBoxControl class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ole.CheckBoxControl class. The CheckBox control toggles a value."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/checkboxcontrol/
---

## CheckBoxControl class

The CheckBox control toggles a value.


### Remarks

It has three possible states: selected, cleared, and neither selected nor cleared,
meaning a combination of on and off states.


**Inheritance:** [CheckBoxControl](./) → [MorphDataControl](../morphdatacontrol/) → [Forms2OleControl](../forms2olecontrol/) → [OleControl](../olecontrol/)

### Properties

| Name | Description |
| --- | --- |
| [back_color](../forms2olecontrol/back_color/) | Gets or sets a background color of the control. The default value depends on a type of the control.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [caption](../forms2olecontrol/caption/) | Gets Caption property of control. Default value is an empty string.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [checked](./checked/) | Gets or sets a boolean value indicating either this [CheckBoxControl](./) is checked or not. The default value is ``False``. |
| [child_nodes](../forms2olecontrol/child_nodes/) | Gets collection of immediate child controls.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [enabled](../forms2olecontrol/enabled/) | Returns ``True`` if control is in enabled state.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [fore_color](../forms2olecontrol/fore_color/) | Gets or sets a foreground color of the control. The default value depends on a type of the control.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [group_name](../forms2olecontrol/group_name/) | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [height](../forms2olecontrol/height/) | Gets or sets a height of the control in points.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [is_forms2_ole_control](../olecontrol/is_forms2_ole_control/) | Returns ``True`` if the control is a [Forms2OleControl](../forms2olecontrol/).<br>(Inherited from [OleControl](../olecontrol/)) |
| [name](../olecontrol/name/) | Gets or sets name of the ActiveX control.<br>(Inherited from [OleControl](../olecontrol/)) |
| [type](./type/) | Gets type of Forms 2.0 control. |
| [value](../forms2olecontrol/value/) | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [width](../forms2olecontrol/width/) | Gets or sets a width of the control in points.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |

### Methods

| Name | Description |
| --- | --- |

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

* module [aspose.words.drawing.ole](../)
* class [MorphDataControl](../morphdatacontrol/)

