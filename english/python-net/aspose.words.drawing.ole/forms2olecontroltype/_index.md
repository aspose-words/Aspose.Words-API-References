---
title: Forms2OleControlType enumeration
linktitle: Forms2OleControlType enumeration
articleTitle: Forms2OleControlType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ole.Forms2OleControlType enumeration. Enumerates types of Forms 2.0 controls."
type: docs
weight: 40
url: /python-net/aspose.words.drawing.ole/forms2olecontroltype/
---

## Forms2OleControlType enumeration

Enumerates types of Forms 2.0 controls.


### Members

| Name | Description |
| --- | --- |
| OPTION_BUTTON | A radio button control. |
| LABEL | A control that displays text. |
| TEXTBOX | A control that allows the user to enter text. |
| CHECK_BOX | A control that allows the user to select or deselect an option. |
| TOGGLE_BUTTON | A control that allows the user to toggle between two states. |
| SPIN_BUTTON | A control that allows the user to increase or decrease a value. |
| COMBO_BOX | A control that allows the user to select an item from a list. |
| FRAME | A control that groups other controls. |
| MULTI_PAGE | A control that displays multiple pages of content. |
| TAB_STRIP | A control that allows the user to switch between multiple pages of content. |
| COMMAND_BUTTON | A button that triggers an action when clicked. |
| IMAGE | A control that displays an image. |
| SCROLL_BAR | A control that allows the user to scroll through content. |
| FORM | A container for other controls. |
| LIST_BOX | A control that displays a list of items. |

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

