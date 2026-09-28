---
title: InlineStory.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /de/python-net/aspose.words/inlinestory/is_insert_revision/
---

## InlineStory.is_insert_revision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```python
@property
def is_insert_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Wenn wir das Dokument bearbeiten, während die Option "Track Changes", zu finden über Review -> Tracking,
# in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
# Beim Bearbeiten eines Dokuments mit Aspose.Words können wir die Verfolgung von Revisionen beginnen, indem wir
# die Methode "StartTrackRevisions" des Dokuments aufrufen und die Verfolgung mit der Methode "StopTrackRevisions" beenden.
# Wir können Revisionen entweder akzeptieren, um sie in das Dokument zu übernehmen
# oder lehnen Sie sie ab, um die vorgeschlagene Änderung rückgängig zu machen und zu verwerfen.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Unten sind fünf Arten von Revisionen aufgeführt, die einen InlineStory‑Knoten kennzeichnen können.
# 1 -  Eine "insert"‑Revision:
# Diese Revision tritt auf, wenn wir Text einfügen, während Änderungen verfolgt werden.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  Eine "move from"‑Revision:
# Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
# während Änderungen verfolgt werden, erscheinen zwei Revisionen.
# Die "move from"‑Revision ist eine Kopie des Textes, wie er ursprünglich vor dem Verschieben war.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  Eine "move to"‑Revision:
# Die "move to"‑Revision ist der Text, den wir an seiner neuen Position im Dokument verschoben haben.
# "Move from"‑ und "move to"‑Revisionen erscheinen paarweise für jede durchgeführte Verschieberevision.
# Das Akzeptieren einer Verschieberevision löscht die "move from"‑Revision und deren Text,
# und behält den Text der "move to"‑Revision bei.
# Das Ablehnen einer Verschieberevision hingegen behält die "move from"‑Revision und löscht die "move to"‑Revision.
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  Eine "delete"‑Revision:
# Diese Revision tritt auf, wenn wir Text löschen, während Änderungen verfolgt werden. Wenn wir Text auf diese Weise löschen,
# bleibt er im Dokument als Revision, bis wir die Revision entweder akzeptieren,
# die den Text dauerhaft löscht, oder die Revision ablehnt, die den gelöschten Text an seiner Stelle belässt.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

