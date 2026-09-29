---
title: RevisionCollection class
linktitle: RevisionCollection class
articleTitle: RevisionCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RevisionCollection class. A collection of [Revision](../revision/) objects that represent revisions in the document"
type: docs
weight: 1060
url: /sv/python-net/aspose.words/revisioncollection/
---

## RevisionCollection class

A collection of [Revision](../revision/) objects that represent revisions in the document.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [Document.revisions](../document/revisions/) property to get revisions present in a document.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [Revision](../revision/) at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of revisions in the collection. |
| [groups](./groups/) | Collection of revision groups. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(criteria)](./accept/#irevisioncriteria) | Accepts revisions that match specified criteria. |
|[ accept_all()](./accept_all/#default) | Accepts all revisions in this collection. |
|[ reject(criteria)](./reject/#irevisioncriteria) | Rejects revisions that match specified criteria. |
|[ reject_all()](./reject_all/#default) | Rejects all revisions in this collection. |

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Normal redigering av dokumentet räknas inte som en revision.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # För att registrera våra redigeringar som revisioner måste vi ange en författare och sedan börja spåra dem.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Denna flagga motsvarar alternativet "Review" -> "Tracking" -> "Track Changes" i Microsoft Word.
        # Metoden "StartTrackRevisions" påverkar inte dess värde,
        # och dokumentet spårar revisioner programmässigt trots att det har värdet "false".
        # Om vi öppnar detta dokument med Microsoft Word kommer det inte att spåra revisioner.
        self.assertFalse(doc.track_revisions)
        # Vi har lagt till text med dokumentbyggaren, så den första revisionen är en insättningsrevision.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Ta bort en körning för att skapa en raderingsrevision.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Att lägga till en ny revision placerar den i början av revisionssamlingen.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Infogningsrevisioner visas i dokumentkroppen redan innan vi accepterar/avvisar revisionen.
        # Att avvisa revisionen kommer att ta bort dess noder från kroppen. Omvänt finns noder som utgör raderingsrevisioner
        # ligger också kvar i dokumentet tills vi accepterar revisionen.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Att acceptera raderingsrevisionen kommer att ta bort dess föräldranod från stycke­texten
        # och sedan ta bort samlingens revision själv.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Flytta nu noden för att skapa en rörlig revisionstyp.
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
        # Den rörliga revisionen är nu på index 1. Avvisa revisionen för att kasta dess innehåll.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

