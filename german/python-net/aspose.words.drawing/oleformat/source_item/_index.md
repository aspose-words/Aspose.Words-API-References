---
title: OleFormat.source_item property
linktitle: source_item property
articleTitle: source_item property
second_title: Aspose.Words for Python
description: "OleFormat.source_item property. Gets or sets a string that is used to identify the portion of the source file that is being linked."
type: docs
weight: 110
url: /de/python-net/aspose.words.drawing/oleformat/source_item/
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
# Betten Sie eine Microsoft Visio-Zeichnung als OLE-Objekt in das Dokument ein.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=False, as_icon=False, presentation=None)
# Fügen Sie einen Link zur Datei im lokalen Dateisystem ein und zeigen Sie ihn als Symbol an.
builder.insert_ole_object(file_name=IMAGE_DIR + 'Microsoft Visio drawing.vsd', prog_id='Package', is_linked=True, as_icon=True, presentation=None)
# Das Einfügen von OLE-Objekten erzeugt Formen, die diese Objekte speichern.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
self.assertEqual(2, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.OLE_OBJECT, shapes))))
# Wenn eine Form ein OLE-Objekt enthält, hat sie eine gültige "OleFormat"-Eigenschaft,
# die wir verwenden können, um einige Aspekte der Form zu überprüfen.
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
# Wenn das Objekt OLE-Daten enthält, können wir über einen Stream darauf zugreifen.
ole_entry_bytes = ole_format.get_ole_entry('\x01CompObj').read()
self.assertEqual(76, len(ole_entry_bytes))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

