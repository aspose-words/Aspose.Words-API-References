---
title: Node.range property
linktitle: range property
articleTitle: range property
second_title: Aspose.Words for Python
description: "Node.range property. Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node."
type: docs
weight: 80
url: /it/python-net/aspose.words/node/range/
---

## Node.range property

Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node.



```python
@property
def range(self) -> aspose.words.Range:
    ...

```

### Examples

Shows how to delete all the nodes from a range.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aggiungi testo alla prima sezione del documento, quindi aggiungi un'altra sezione.
builder.write('Section 1. ')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.write('Section 2.')
self.assertEqual('Section 1. \x0cSection 2.', doc.get_text().strip())
# Rimuovi completamente la prima sezione eliminando tutti i nodi
# all'interno del suo intervallo, inclusa la sezione stessa.
doc.sections[0].range.delete()
self.assertEqual(1, doc.sections.count)
self.assertEqual('Section 2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

