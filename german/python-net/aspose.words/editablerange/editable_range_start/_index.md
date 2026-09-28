---
title: EditableRange.editable_range_start property
linktitle: editable_range_start property
articleTitle: editable_range_start property
second_title: Aspose.Words for Python
description: "EditableRange.editable_range_start property. Gets the node that represents the start of the editable range."
type: docs
weight: 20
url: /de/python-net/aspose.words/editablerange/editable_range_start/
---

## EditableRange.editable_range_start property

Gets the node that represents the start of the editable range.


```python
@property
def editable_range_start(self) -> aspose.words.EditableRangeStart:
    ...

```

### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# Editierbare Bereiche ermöglichen es uns, Teile geschützter Dokumente zum Bearbeiten freizugeben.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# Ein korrekt formatierter editierbarer Bereich hat einen Startknoten und einen Endknoten.
# Diese Knoten besitzen passende IDs und umfassen editierbare Knoten.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Verschiedene Teile des editierbaren Bereichs verlinken miteinander.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Wir können die Knotentypen jedes Teils wie folgt abrufen. Der editierbare Bereich selbst ist kein Knoten,
# sondern ein Objekt, das aus einem Start, einem Ende und deren eingeschlossenen Inhalten besteht.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Entfernen Sie einen editierbaren Bereich. Alle Knoten, die sich innerhalb des Bereichs befanden, bleiben unverändert erhalten.
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRange](../)

