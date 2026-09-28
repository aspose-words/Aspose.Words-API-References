---
title: Node.range property
linktitle: range property
articleTitle: range property
second_title: Aspose.Words for Python
description: "Node.range property. Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node."
type: docs
weight: 80
url: /de/python-net/aspose.words/node/range/
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
# Fügen Sie dem ersten Abschnitt im Dokument Text hinzu und fügen Sie dann einen weiteren Abschnitt hinzu.
builder.write('Section 1. ')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.write('Section 2.')
self.assertEqual('Section 1. \x0cSection 2.', doc.get_text().strip())
# Entfernen Sie den ersten Abschnitt vollständig, indem Sie alle Knoten entfernen
# innerhalb seines Bereichs, einschließlich des Abschnitts selbst.
doc.sections[0].range.delete()
self.assertEqual(1, doc.sections.count)
self.assertEqual('Section 2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

