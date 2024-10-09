---
title: CommandButtonControl class
linktitle: CommandButtonControl class
articleTitle: CommandButtonControl class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ole.CommandButtonControl class. The CommandButton control runs a macro that performs an action when a user clicks it."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/commandbuttoncontrol/
---

## CommandButtonControl class

The CommandButton control runs a macro that performs an action when a user clicks it.


**Inheritance:** [CommandButtonControl](./) → [Forms2OleControl](../forms2olecontrol/) → [OleControl](../olecontrol/)

### Constructors
| Name | Description |
| --- | --- |
| [CommandButtonControl()](./__init__/#default) | Initializes a new instance of [CommandButtonControl](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [back_color](../forms2olecontrol/back_color/) | Gets or sets a background color of the control. The default value depends on a type of the control.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
| [caption](../forms2olecontrol/caption/) | Gets Caption property of control. Default value is an empty string.<br>(Inherited from [Forms2OleControl](../forms2olecontrol/)) |
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

Shows how to insert ActiveX control.

```python
builder = aw.DocumentBuilder()
button1 = aw.drawing.ole.CommandButtonControl()
shape = builder.insert_forms_2_ole_control(button1)
self.assertEqual(aw.drawing.ole.Forms2OleControlType.COMMAND_BUTTON, shape.ole_format.ole_control.as_forms2_ole_control().type)
```

### See Also

* module [aspose.words.drawing.ole](../)
* class [Forms2OleControl](../forms2olecontrol/)

