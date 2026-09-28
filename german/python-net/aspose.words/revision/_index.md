---
title: Revision class
linktitle: Revision class
articleTitle: Revision class
second_title: Aspose.Words for Python
description: "aspose.words.Revision class. Represents a revision (tracked change) in a document node or style"
type: docs
weight: 1050
url: /de/python-net/aspose.words/revision/
---

## Revision class

Represents a revision (tracked change) in a document node or style.
Use [Revision.revision_type](./revision_type/) to check the type of this revision.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the author of this revision. Can not be empty string or ``None``. |
| [date_time](./date_time/) | Gets or sets the date/time of this revision. |
| [group](./group/) | Gets the revision group. Returns ``None`` if the revision does not belong to any group. |
| [parent_node](./parent_node/) | Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE). |
| [parent_style](./parent_style/) | Gets the immediate parent style (owner) of this revision. This property will work for only for the [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE) revision type. |
| [revision_type](./revision_type/) | Gets the type of this revision. |

### Methods

| Name | Description |
| --- | --- |
|[ accept()](./accept/#default) | Accepts this revision. |
|[ reject()](./reject/#default) | Reject this revision. |

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Normale Bearbeitung des Dokuments wird nicht als Revision gezählt.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Um unsere Änderungen als Revisionen zu registrieren, müssen wir einen Autor festlegen und dann mit der Verfolgung beginnen.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Dieses Flag entspricht der Option "Review" -> "Tracking" -> "Track Changes" in Microsoft Word.
        # Die Methode "StartTrackRevisions" beeinflusst ihren Wert nicht,
        # und das Dokument verfolgt Revisionen programmgesteuert, obwohl es den Wert "false" hat.
        # Wenn wir dieses Dokument mit Microsoft Word öffnen, wird es keine Revisionen verfolgen.
        self.assertFalse(doc.track_revisions)
        # Wir haben Text mit dem Dokument‑Builder hinzugefügt, sodass die erste Revision eine Einfüge‑Revision ist.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Entfernen Sie einen Lauf, um eine Lösch‑Revision zu erzeugen.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Hinzufügen einer neuen Revision platziert sie am Anfang der Revisionssammlung.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Einfüge‑Revisionen erscheinen im Dokumentkörper, noch bevor wir die Revision annehmen/ablehnen.
        # Das Ablehnen der Revision entfernt ihre Knoten aus dem Body. Umgekehrt verbleiben Knoten, die Löschrevisionen bilden
        # bleiben ebenfalls im Dokument, bis wir die Revision akzeptieren.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Das Akzeptieren der Löschrevision entfernt ihren übergeordneten Knoten aus dem Absatztext
        # und anschließend wird die Revision der Sammlung selbst entfernt.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Verschieben Sie jetzt den Knoten, um einen bewegten Revisionstyp zu erstellen.
        node = doc.first_section.body.paragraphs[1]
        end_node = doc.first_section.body.paragraphs[1].next_sibling
        reference_node = doc.first_section.body.paragraphs[0]
        while node != end_node:
            next_node = node.next_sibling
            doc.first_section.body.insert_before(node, reference_node)
            node = next_node
        self.assertEqual(aw.RevisionType.MOVING, doc.revisions[0].revision_type)
        self.assertEqual(8, doc.revisions.count)
        self.assertEqual('This is revision #2.\rThis is revision #1. \rThis is revision #2.', doc.get_text().strip())
        # Die bewegte Revision befindet sich jetzt bei Index 1. Lehnen Sie die Revision ab, um ihren Inhalt zu verwerfen.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

