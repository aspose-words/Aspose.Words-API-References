---
title: EditableRangeStart.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "EditableRangeStart.node_type property. Returns [NodeType.EDITABLE_RANGE_START](../../nodetype/#EDITABLE_RANGE_START)."
type: docs
weight: 30
url: /fr/python-net/aspose.words/editablerangestart/node_type/
---

## EditableRangeStart.node_type property

Returns [NodeType.EDITABLE_RANGE_START](../../nodetype/#EDITABLE_RANGE_START).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# Les plages éditables nous permettent de laisser certaines parties de documents protégés ouvertes à l'édition.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# Une plage éditable bien formée possède un nœud de début et un nœud de fin.
# Ces nœuds ont des ID correspondants et englobent des nœuds éditables.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Différentes parties de la plage éditable sont liées entre elles.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Nous pouvons accéder aux types de nœuds de chaque partie ainsi. La plage éditable elle‑même n'est pas un nœud,
# mais une entité qui consiste en un début, une fin et leur contenu inclus.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Supprimer une plage éditable. Tous les nœuds qui se trouvaient à l'intérieur de la plage resteront intacts.
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRangeStart](../)

