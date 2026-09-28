---
title: Inline.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "Inline.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 50
url: /de/python-net/aspose.words/inline/is_move_from_revision/
---

## Inline.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Wenn wir das Dokument bearbeiten, während die Option "Track Changes", zu finden über Review -> Tracking,
# in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
# Beim Bearbeiten eines Dokuments mit Aspose.Words können wir die Verfolgung von Revisionen beginnen, indem wir
# die Methode "StartTrackRevisions" des Dokuments aufrufen und die Verfolgung mit der Methode "StopTrackRevisions" beenden.
# Wir können Revisionen entweder akzeptieren, um sie in das Dokument zu übernehmen
# oder sie ablehnen, um die vorgeschlagene Änderung wirksam zu entfernen.
self.assertEqual(6, doc.revisions.count)
# Der übergeordnete Knoten einer Revision ist der Run, auf den sich die Revision bezieht. Ein Run ist ein Inline‑Knoten.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Unten sind fünf Arten von Revisionen aufgeführt, die einen Inline‑Knoten kennzeichnen können.
# 1 -  Eine "insert"‑Revision:
# Diese Revision tritt auf, wenn wir Text einfügen, während Änderungen verfolgt werden.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Eine "format"‑Revision:
# Diese Revision tritt auf, wenn wir die Formatierung von Text ändern, während Änderungen verfolgt werden.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Eine "move from"‑Revision:
# Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
# während Änderungen verfolgt werden, erscheinen zwei Revisionen.
# Die "move from"‑Revision ist eine Kopie des Textes, wie er ursprünglich vor dem Verschieben war.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Eine "move to"‑Revision:
# Die "move to"‑Revision ist der Text, den wir an seiner neuen Position im Dokument verschoben haben.
# "Move from"‑ und "move to"‑Revisionen erscheinen paarweise für jede durchgeführte Verschieberevision.
# Das Akzeptieren einer Verschieberevision löscht die "move from"‑Revision und deren Text,
# und behält den Text der "move to"‑Revision bei.
# Das Ablehnen einer Verschieberevision hingegen behält die "move from"‑Revision und löscht die "move to"‑Revision.
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Eine "delete"‑Revision:
# Diese Revision tritt auf, wenn wir Text löschen, während Änderungen verfolgt werden. Wenn wir Text auf diese Weise löschen,
# bleibt er im Dokument als Revision, bis wir die Revision entweder akzeptieren,
# die den Text dauerhaft löscht, oder die Revision ablehnt, die den gelöschten Text an seiner Stelle belässt.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [Inline](../)

