---
title: DocumentBuilder.start_editable_range method
linktitle: start_editable_range method
articleTitle: start_editable_range method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_editable_range method. Marks the current position in the document as an editable range start."
type: docs
weight: 670
url: /it/python-net/aspose.words/documentbuilder/start_editable_range/
---

## start_editable_range() {#default}

Marks the current position in the document as an editable range start.


```python
def start_editable_range(self):
    ...
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](./#default) and [DocumentBuilder.end_editable_range()](../end_editable_range/#default)
or [DocumentBuilder.end_editable_range()](../end_editable_range/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# Gli intervalli modificabili ci permettono di lasciare parti di documenti protetti aperti per la modifica.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# Un intervallo modificabile ben formato ha un nodo di inizio e un nodo di fine.
# Questi nodi hanno ID corrispondenti e includono nodi modificabili.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Parti diverse dell'intervallo modificabile sono collegate tra loro.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Possiamo accedere ai tipi di nodo di ogni parte in questo modo. L'intervallo modificabile stesso non è un nodo,
# ma un'entità che consiste in un inizio, una fine e i loro contenuti racchiusi.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Rimuovi un intervallo modificabile. Tutti i nodi che erano all'interno dell'intervallo rimarranno intatti.
editable_range.remove()
```

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " + 'we cannot edit this paragraph without the password.')
# Crea due intervalli modificabili annidati.
outer_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside the outer editable range and can be edited.')
inner_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside both the outer and inner editable ranges and can be edited.')
# Attualmente, il cursore di inserimento dei nodi del document builder si trova in più di un intervallo modificabile in corso.
# Quando vogliamo terminare un intervallo modificabile in questa situazione,
# dobbiamo specificare quale degli intervalli desideriamo terminare passando il suo nodo EditableRangeStart.
builder.end_editable_range(inner_editable_range_start)
builder.writeln('This paragraph inside the outer editable range and can be edited.')
builder.end_editable_range(outer_editable_range_start)
builder.writeln('This paragraph is outside any editable ranges, and cannot be edited.')
# Se una regione di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
# il gruppo combinato di utenti esclusi da entrambi i gruppi è impedito dal modificarlo.
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.Nested.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

