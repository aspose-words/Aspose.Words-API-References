---
title: OleFormat.source_item property
linktitle: source_item property
articleTitle: source_item property
second_title: Aspose.Words for Python
description: "OleFormat.source_item property. Gets or sets a string that is used to identify the portion of the source file that is being linked."
type: docs
weight: 110
url: /tr/python-net/aspose.words.drawing/oleformat/source_item/
---

## OleFormat.source_item property

Gets or sets a string that is used to identify the portion of the source file that is being linked.


```python
@property
def source_item(self) -> str:
    ...

@source_item.setter
def source_item(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [OleFormat.source_item](./)
property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from
the worksheet.




### Examples

Shows how to insert linked and unlinked OLE objects.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Microsoft Visio çizimini belgeye OLE nesnesi olarak gömün.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=False, as_icon=False, presentation=None)
# Yerel dosya sistemindeki dosyaya bir bağlantı ekleyin ve simge olarak gösterin.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=True, as_icon=True, presentation=None)
# OLE nesnelerini eklemek, bu nesneleri depolayan şekiller oluşturur.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
self.assertEqual(2, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.OLE_OBJECT, shapes))))
# Bir şekil OLE nesnesi içeriyorsa, geçerli bir "OleFormat" özelliğine sahip olacaktır,
# bu özelliği şeklin bazı yönlerini doğrulamak için kullanabiliriz.
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
# Nesne OLE verisi içeriyorsa, ona bir akış kullanarak erişebiliriz.
ole_entry_bytes = ole_format.get_ole_entry('\x01CompObj').read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

