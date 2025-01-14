---
title: CommandButtonControl constructor
linktitle: CommandButtonControl constructor
articleTitle: CommandButtonControl constructor
second_title: Aspose.Words for Python
description: "CommandButtonControl constructor. Initializes a new instance of [CommandButtonControl](../) class."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.ole/commandbuttoncontrol/__init__/
---

## CommandButtonControl() {#default}

Initializes a new instance of [CommandButtonControl](../) class.



```python
def __init__(self):
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

