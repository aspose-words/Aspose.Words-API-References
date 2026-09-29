---
title: OleFormat.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "OleFormat.source_full_name property. Gets or sets the path and name of the source file for the linked OLE object."
type: docs
weight: 100
url: /ru/python-net/aspose.words.drawing/oleformat/source_full_name/
---

## OleFormat.source_full_name property

Gets or sets the path and name of the source file for the linked OLE object.


```python
@property
def source_full_name(self) -> str:
    ...

@source_full_name.setter
def source_full_name(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

If [OleFormat.source_full_name](./) is not an empty string, the OLE object is linked.




### Examples

Shows how to insert linked and unlinked OLE objects.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте рисунок Microsoft Visio в документ в виде OLE‑объекта.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=False, as_icon=False, presentation=None)
# Вставьте ссылку на файл в локальной файловой системе и отобразите её как значок.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=True, as_icon=True, presentation=None)
# Вставка OLE‑объектов создаёт фигуры, которые хранят эти объекты.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
self.assertEqual(2, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.OLE_OBJECT, shapes))))
# Если фигура содержит OLE‑объект, у неё будет действительное свойство "OleFormat",
# которое мы можем использовать для проверки некоторых аспектов фигуры.
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
# Если объект содержит OLE‑данные, мы можем получить к ним доступ с помощью потока.
ole_entry_bytes = ole_format.get_ole_entry('\x01CompObj').read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

