---
title: OptionButtonControl.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "OptionButtonControl.type property. Gets type of Forms 2.0 control."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---

## OptionButtonControl.type property

Gets type of Forms 2.0 control.


```python
@property
def type(self) -> aspose.words.drawing.ole.Forms2OleControlType:
    ...

```

### Examples

Shows how to select radio button.

```python
doc = aw.Document(file_name=MY_DIR + 'Radio buttons.docx')
shape1 = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
option_button1 = shape1.ole_format.ole_control.as_option_button_control()
# Deselect selected first item.
option_button1.selected = False
shape2 = doc.get_child(aw.NodeType.SHAPE, 1, True).as_shape()
option_button2 = shape2.ole_format.ole_control.as_option_button_control()
# Select second option button.
option_button2.selected = True
self.assertEqual(aw.drawing.ole.Forms2OleControlType.OPTION_BUTTON, option_button1.type)
self.assertEqual(aw.drawing.ole.Forms2OleControlType.OPTION_BUTTON, option_button2.type)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.SelectRadioControl.docx')
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [OptionButtonControl](../)

