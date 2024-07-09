---
title: OptionButtonControl.selected property
linktitle: selected property
articleTitle: selected property
second_title: Aspose.Words for Python
description: "OptionButtonControl.selected property. Gets or sets a boolean value indicating either this [OptionButtonControl](../) is selected or not."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---

## OptionButtonControl.selected property

Gets or sets a boolean value indicating either this [OptionButtonControl](../) is selected or not.



```python
@property
def selected(self) -> bool:
    ...

@selected.setter
def selected(self, value: bool):
    ...

```

### Remarks

Note, this property allows you to select multiple items in a group of [OptionButtonControl](../)
with the same [Forms2OleControl.group_name](../../forms2olecontrol/group_name/). It is up to you to take care of deselecting a previously
selected item when you make this [OptionButtonControl](../) selected.



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
doc.save(file_name=ARTIFACTS_DIR + 'Shape.SelectRadioControl.docx')
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [OptionButtonControl](../)

