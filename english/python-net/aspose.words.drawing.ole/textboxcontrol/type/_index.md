---
title: TextBoxControl.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "TextBoxControl.type property. Gets type of Forms 2.0 control."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/textboxcontrol/type/
---

## TextBoxControl.type property

Gets type of Forms 2.0 control.


```python
@property
def type(self) -> aspose.words.drawing.ole.Forms2OleControlType:
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
self.assertEqual(aw.drawing.ole.Forms2OleControlType.TEXTBOX, text_box_control.type)
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [TextBoxControl](../)

