---
title: OleFormat.is_link property
linktitle: is_link property
articleTitle: is_link property
second_title: Aspose.Words for Python
description: "OleFormat.is_link property. Returns ``True`` if the OLE object is linked (when [OleFormat.source_full_name](../source_full_name/) is specified)."
type: docs
weight: 40
url: /it/python-net/aspose.words.drawing/oleformat/is_link/
---

## OleFormat.is_link property

Returns ``True`` if the OLE object is linked (when [OleFormat.source_full_name](../source_full_name/) is specified).



```python
@property
def is_link(self) -> bool:
    ...

```

### Examples

Shows how to insert linked and unlinked OLE objects.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un disegno Microsoft Visio nel documento come oggetto OLE.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=False, as_icon=False, presentation=None)
# Inserisci un collegamento al file nel file system locale e visualizzalo come icona.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=True, as_icon=True, presentation=None)
# L'inserimento di oggetti OLE crea forme che memorizzano questi oggetti.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
self.assertEqual(2, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.OLE_OBJECT, shapes))))
# Se una forma contiene un oggetto OLE, avrà una proprietà "OleFormat" valida,
# che possiamo usare per verificare alcuni aspetti della forma.
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
# Se l'oggetto contiene dati OLE, possiamo accedervi usando uno stream.
ole_entry_bytes = ole_format.get_ole_entry('\x01CompObj').read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

