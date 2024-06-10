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
doc = aw.Document(file_name=MY_DIR + 'Textbox control.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
text_box_control = shape.ole_format.ole_control.as_text_box_control()
self.assertEqual('Aspose.Words test', text_box_control.text)
text_box_control.text = 'Updated text'
self.assertEqual('Updated text', text_box_control.text)
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [TextBoxControl](../)

