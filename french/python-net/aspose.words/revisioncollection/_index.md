---
title: RevisionCollection class
linktitle: RevisionCollection class
articleTitle: RevisionCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RevisionCollection class. A collection of [Revision](../revision/) objects that represent revisions in the document"
type: docs
weight: 1060
url: /fr/python-net/aspose.words/revisioncollection/
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
        # La modification normale du document ne compte pas comme une révision.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Pour enregistrer nos modifications en tant que révisions, nous devons déclarer un auteur, puis commencer à les suivre.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Ce drapeau correspond à l'option "Révision" -> "Suivi" -> "Suivre les modifications" dans Microsoft Word.
        # La méthode "StartTrackRevisions" n'affecte pas sa valeur,
        # et le document suit les révisions de manière programmatique malgré le fait qu'il ait la valeur "false".
        # Si nous ouvrons ce document avec Microsoft Word, il ne suivra pas les révisions.
        self.assertFalse(doc.track_revisions)
        # Nous avons ajouté du texte à l'aide du constructeur de document, donc la première révision est une révision de type insertion.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Supprimez une exécution pour créer une révision de type suppression.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # L'ajout d'une nouvelle révision la place au début de la collection de révisions.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Les révisions d'insertion apparaissent dans le corps du document même avant que nous acceptions/rejetions la révision.
        # Rejeter la révision supprimera ses nœuds du corps. Inversement, les nœuds qui composent les révisions de suppression
        # persistent également dans le document jusqu'à ce que nous acceptions la révision.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Accepter la révision de suppression supprimera son nœud parent du texte du paragraphe
        # et supprimera ensuite la révision de la collection elle-même.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Déplacez maintenant le nœud pour créer un type de révision mobile.
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
        # La révision mobile est maintenant à l'index 1. Rejetez la révision pour en supprimer le contenu.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

