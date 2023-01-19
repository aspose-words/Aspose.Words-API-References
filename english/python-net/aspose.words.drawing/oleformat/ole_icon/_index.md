---
title: ole_icon property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the draw aspect of the OLE object"
type: docs
weight: 70
url: /python-net/aspose.words.drawing/oleformat/ole_icon/
---

## OleFormat.ole_icon property

Gets the draw aspect of the OLE object. When ``True``, the OLE object is displayed as an icon.
When ``False``, the OLE object is displayed as content.


Aspose.Words does not allow to set this property to avoid confusion. If you were able to change
the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original
draw aspect until you edit or update the OLE object in Microsoft Word.




### Examples

Shows how to insert linked and unlinked OLE objects.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Embed a Microsoft Visio drawing into the document as an OLE object.
builder.insert_ole_object(IMAGE_DIR + "Microsoft Visio drawing.vsd", "Package", False, False, None)

# Insert a link to the file in the local file system and display it as an icon.
builder.insert_ole_object(IMAGE_DIR + "Microsoft Visio drawing.vsd", "Package", True, True, None)

# Inserting OLE objects creates shapes that store these objects.
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]

self.assertEqual(2, len(shapes))
self.assertEqual(2, len([shape for shape in shapes if shape.shape_type == aw.drawing.ShapeType.OLE_OBJECT]))

# If a shape contains an OLE object, it will have a valid "ole_format" property,
# which we can use to verify some aspects of the shape.
ole_format = shapes[0].ole_format

self.assertEqual(False, ole_format.is_link)
self.assertEqual(False, ole_format.ole_icon)

ole_format = shapes[1].ole_format

self.assertEqual(True, ole_format.is_link)
self.assertEqual(True, ole_format.ole_icon)

self.assertTrue(ole_format.source_full_name.endswith("Images/Microsoft Visio drawing.vsd"))
self.assertEqual("", ole_format.source_item)

self.assertEqual("Microsoft Visio drawing.vsd", ole_format.icon_caption)

doc.save(ARTIFACTS_DIR + "Shape.ole_links.docx")

# If the object contains OLE data, we can access it using a stream.
stream = ole_format.get_ole_entry("\u0001CompObj")
stream.seek(0)
ole_entry_bytes = stream.read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

