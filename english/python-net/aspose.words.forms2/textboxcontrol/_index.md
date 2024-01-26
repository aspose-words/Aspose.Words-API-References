---
title: TextBoxControl class
linktitle: TextBoxControl class
articleTitle: TextBoxControl class
second_title: Aspose.Words for Python
description: "aspose.words.forms2.TextBoxControl class. The TextBox control displays text from an organized set of data or user input."
type: docs
weight: 20
url: /python-net/aspose.words.forms2/textboxcontrol/
---

## TextBoxControl class

The TextBox control displays text from an organized set of data or user input.


**Inheritance:** [TextBoxControl](./) → [MorphDataControl](../morphdatacontrol/) → [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/) → [OleControl](../../aspose.words.drawing.ole/olecontrol/)

### Properties

| Name | Description |
| --- | --- |
| [caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) | Gets Caption property of control. Default value is an empty string.<br>(Inherited from [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)) |
| [child_nodes](../../aspose.words.drawing.ole/forms2olecontrol/child_nodes/) | Gets collection of immediate child controls.<br>(Inherited from [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)) |
| [enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) | Returns ``True`` if control is in enabled state.<br>(Inherited from [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)) |
| [group_name](../../aspose.words.drawing.ole/forms2olecontrol/group_name/) | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string.<br>(Inherited from [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)) |
| [is_forms2_ole_control](../../aspose.words.drawing.ole/olecontrol/is_forms2_ole_control/) | Returns ``True`` if the control is a [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/).<br>(Inherited from [OleControl](../../aspose.words.drawing.ole/olecontrol/)) |
| [name](../../aspose.words.drawing.ole/olecontrol/name/) | Gets or sets name of the ActiveX control.<br>(Inherited from [OleControl](../../aspose.words.drawing.ole/olecontrol/)) |
| [text](./text/) | Gets or sets a text of the control. |
| [type](./type/) | Gets type of Forms 2.0 control. |
| [value](../../aspose.words.drawing.ole/forms2olecontrol/value/) | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string.<br>(Inherited from [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)) |

### Methods

| Name | Description |
| --- | --- |

### Examples

Shows how to change text of the TextBox OLE control.

```python
doc = aw.Document(MY_DIR + "Textbox control.docm")

shape = doc.get_child(NodeType.SHAPE, 0, True).as_shape()

textBoxControl = shape.ole_format.ole_control.as_forms2_ole_control().as_text_box_control()
self.assertEqual("Aspose.Words test", textBoxControl.text)

textBoxControl.text = "Updated text"
self.assertEqual("Updated text", textBoxControl.text)
```

### See Also

* module [aspose.words.forms2](../)
* class [MorphDataControl](../morphdatacontrol/)

