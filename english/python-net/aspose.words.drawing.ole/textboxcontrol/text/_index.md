---
title: TextBoxControl.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "TextBoxControl.text property. Gets or sets a text of the control."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/textboxcontrol/text/
---

## TextBoxControl.text property

Gets or sets a text of the control.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

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

* module [aspose.words.drawing.ole](../../)
* class [TextBoxControl](../)

