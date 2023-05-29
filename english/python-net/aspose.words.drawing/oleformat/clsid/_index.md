---
title: OleFormat.clsid property
linktitle: clsid property
articleTitle: clsid property
second_title: Aspose.Words for Python
description: "OleFormat.clsid property. Gets the CLSID of the OLE object."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/oleformat/clsid/
---

## OleFormat.clsid property

Gets the CLSID of the OLE object.


### Examples

Shows how to access an OLE control embedded in a document and its child controls.

```python
doc = aw.Document(MY_DIR + "OLE ActiveX controls.docm")

# Shapes store and display OLE objects in the document's body.
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

self.assertEqual("6e182020-f460-11ce-9bcd-00aa00608e01", str(shape.ole_format.clsid))

ole_control = shape.ole_format.ole_control.as_forms2_ole_control()

# Some OLE controls may contain child controls, such as the one in this document with three options buttons.
ole_control_collection = ole_control.child_nodes

self.assertEqual(3, ole_control_collection.count)

self.assertEqual("C#", ole_control_collection[0].caption)
self.assertEqual("1", ole_control_collection[0].value)

self.assertEqual("Visual Basic", ole_control_collection[1].caption)
self.assertEqual("0", ole_control_collection[1].value)

self.assertEqual("Delphi", ole_control_collection[2].caption)
self.assertEqual("0", ole_control_collection[2].value)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

