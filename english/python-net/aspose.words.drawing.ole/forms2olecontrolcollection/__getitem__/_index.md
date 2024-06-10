---
title: Forms2OleControlCollection indexer
linktitle: Forms2OleControlCollection indexer
articleTitle: Forms2OleControlCollection indexer
second_title: Aspose.Words for Python
description: "Forms2OleControlCollection indexer. Gets [Forms2OleControl](../../forms2olecontrol/) object at a specified index."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.ole/forms2olecontrolcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets [Forms2OleControl](../../forms2olecontrol/) object at a specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to access an OLE control embedded in a document and its child controls.

```python
doc = aw.Document(MY_DIR + 'OLE ActiveX controls.docm')
# Shapes store and display OLE objects in the document's body.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual('6e182020-f460-11ce-9bcd-00aa00608e01', str(shape.ole_format.clsid))
ole_control = shape.ole_format.ole_control.as_forms2_ole_control()
# Some OLE controls may contain child controls, such as the one in this document with three options buttons.
ole_control_collection = ole_control.child_nodes
self.assertEqual(3, ole_control_collection.count)
self.assertEqual('C#', ole_control_collection[0].caption)
self.assertEqual('1', ole_control_collection[0].value)
self.assertEqual('Visual Basic', ole_control_collection[1].caption)
self.assertEqual('0', ole_control_collection[1].value)
self.assertEqual('Delphi', ole_control_collection[2].caption)
self.assertEqual('0', ole_control_collection[2].value)
```

### See Also

* module [aspose.words.drawing.ole](../../)
* class [Forms2OleControlCollection](../)

