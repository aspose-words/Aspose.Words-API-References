---
title: OleFormat.ole_icon property
linktitle: ole_icon property
articleTitle: ole_icon property
second_title: Aspose.Words for Python
description: "OleFormat.ole_icon property. Gets the draw aspect of the OLE object"
type: docs
weight: 70
url: /python-net/aspose.words.drawing/oleformat/ole_icon/
---

## OleFormat.ole_icon property

Gets the draw aspect of the OLE object. When ``True``, the OLE object is displayed as an icon.
When ``False``, the OLE object is displayed as content.



```python
@property
def ole_icon(self) -> bool:
    ...

```

### Remarks

Aspose.Words does not allow to set this property to avoid confusion. If you were able to change
the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original
draw aspect until you edit or update the OLE object in Microsoft Word.




### Examples

Shows how to insert linked and unlinked OLE objects.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Embed a Microsoft Visio drawing into the document as an OLE object.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=False, as_icon=False, presentation=None)
# Insert a link to the file in the local file system and display it as an icon.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=True, as_icon=True, presentation=None)
# Inserting OLE objects creates shapes that store these objects.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
self.assertEqual(2, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.OLE_OBJECT, shapes))))
# If a shape contains an OLE object, it will have a valid "OleFormat" property,
# which we can use to verify some aspects of the shape.
ole_format = shapes[0].ole_format
self.assertEqual(False, ole_format.is_link)
self.assertEqual(False, ole_format.ole_icon)
ole_format = shapes[1].ole_format
self.assertEqual(True, ole_format.is_link)
self.assertEqual(True, ole_format.ole_icon)
assert ole_format.source_full_name.endswith(str(Path(IMAGE_DIR) / 'Microsoft Visio drawing.vsd'))
self.assertEqual('', ole_format.source_item)
self.assertEqual('Microsoft Visio drawing.vsd', ole_format.icon_caption)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.OleLinks.docx')
# If the object contains OLE data, we can access it using a stream.
ole_entry_bytes = ole_format.get_ole_entry('\x01CompObj').read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

