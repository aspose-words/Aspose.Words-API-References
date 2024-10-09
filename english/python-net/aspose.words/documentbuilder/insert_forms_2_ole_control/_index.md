---
title: DocumentBuilder.insert_forms_2_ole_control method
linktitle: insert_forms_2_ole_control method
articleTitle: insert_forms_2_ole_control method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_forms_2_ole_control method. Inserts [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/) object into current position."
type: docs
weight: 350
url: /python-net/aspose.words/documentbuilder/insert_forms_2_ole_control/
---

## insert_forms_2_ole_control(forms_2_ole_control) {#forms2olecontrol}

Inserts [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/) object into current position.



```python
def insert_forms_2_ole_control(self, forms_2_ole_control: aspose.words.drawing.ole.Forms2OleControl):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| forms_2_ole_control | [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/) |  |

### Returns

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)



### Examples

Shows how to insert ActiveX control.

```python
builder = aw.DocumentBuilder()
button1 = aw.drawing.ole.CommandButtonControl()
shape = builder.insert_forms_2_ole_control(button1)
self.assertEqual(aw.drawing.ole.Forms2OleControlType.COMMAND_BUTTON, shape.ole_format.ole_control.as_forms2_ole_control().type)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)
* property [Shape.ole_format](../../../aspose.words.drawing/shape/ole_format/)
* property [OleFormat.ole_control](../../../aspose.words.drawing/oleformat/ole_control/)

