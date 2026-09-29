---
title: EditableRange class
linktitle: EditableRange class
articleTitle: EditableRange class
second_title: Aspose.Words for Python
description: "aspose.words.EditableRange class. Represents a single editable range"
type: docs
weight: 360
url: /sv/python-net/aspose.words/editablerange/
---

## EditableRange class

Represents a single editable range.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRange.editable_range_start](./editable_range_start/)
and [EditableRange.editable_range_end](./editable_range_end/) in a document tree and allows to work with an editable range as a single object.




### Properties

| Name | Description |
| --- | --- |
| [editable_range_end](./editable_range_end/) | Gets the node that represents the end of the editable range. |
| [editable_range_start](./editable_range_start/) | Gets the node that represents the start of the editable range. |
| [editor_group](./editor_group/) | Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [id](./id/) | Gets the editable range identifier. |
| [single_user](./single_user/) | Returns or sets the single user for editable range. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes the editable range from the document. Does not remove content inside the editable range. |

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

* module [aspose.words](../)

