---
title: CommandButtonControl.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "CommandButtonControl.type property. Gets type of Forms 2.0 control."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---

## CommandButtonControl.type property

Gets type of Forms 2.0 control.


```python
@property
def type(self) -> aspose.words.drawing.ole.Forms2OleControlType:
    ...

```

### Examples

Shows how to insert ActiveX control.

```python
builder = aw.DocumentBuilder()
button1 = aw.drawing.ole.CommandButtonControl()
shape = builder.insert_forms_2_ole_control(button1)
self.assertEqual(aw.drawing.ole.Forms2OleControlType.COMMAND_BUTTON, button1.type)
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [CommandButtonControl](../)

