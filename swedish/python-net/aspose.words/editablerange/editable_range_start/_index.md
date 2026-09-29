---
title: EditableRange.editable_range_start property
linktitle: editable_range_start property
articleTitle: editable_range_start property
second_title: Aspose.Words for Python
description: "EditableRange.editable_range_start property. Gets the node that represents the start of the editable range."
type: docs
weight: 20
url: /sv/python-net/aspose.words/editablerange/editable_range_start/
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
# Redigerbara områden låter oss lämna delar av skyddade dokument öppna för redigering.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# Ett välformulerat redigerbart område har en startnod och en slutnod.
# Dessa noder har matchande ID:n och omfattar redigerbara noder.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Olika delar av det redigerbara området länkar till varandra.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Vi kan komma åt nodtyperna för varje del på detta sätt. Det redigerbara området i sig är inte en nod,
# utan en entitet som består av en start, ett slut och deras omslutna innehåll.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Ta bort ett redigerbart område. Alla noder som var inom området kommer att förbli intakta.
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRange](../)

