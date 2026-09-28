---
title: CompositeNode.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "CompositeNode.count property. Gets the number of immediate children of this node."
type: docs
weight: 10
url: /de/python-net/aspose.words/compositenode/count/
---

## CompositeNode.count property

Gets the number of immediate children of this node.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# Ein leeres Dokument hat standardmäßig einen Absatz.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Zusammengesetzte Knoten wie unser Absatz können andere zusammengesetzte und Inline-Knoten als Kinder enthalten.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Erstellen Sie drei weitere Laufknoten.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# Der Dokumentkörper wird diese Läufe nicht anzeigen, bis wir sie in einen zusammengesetzten Knoten einfügen
# der selbst Teil des Knotensbaums des Dokuments ist, wie wir es beim ersten Lauf getan haben.
# Wir können bestimmen, wo der Textinhalt von Knoten, die wir einfügen,
# im Dokument erscheint, indem wir einen Einfügeort relativ zu einem anderen Knoten im Absatz angeben.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Fügen Sie den zweiten Lauf in den Absatz vor dem ursprünglichen Lauf ein.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Fügen Sie den dritten Lauf nach dem ursprünglichen Lauf ein.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Fügen Sie den ersten Lauf am Anfang der Kindknoten‑Sammlung des Absatzes ein.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# Wir können den Inhalt des Laufs ändern, indem wir vorhandene Kindknoten bearbeiten und löschen.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

