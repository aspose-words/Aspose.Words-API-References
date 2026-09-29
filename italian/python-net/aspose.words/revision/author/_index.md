---
title: Revision.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Python
description: "Revision.author property. Gets or sets the author of this revision"
type: docs
weight: 10
url: /it/python-net/aspose.words/revision/author/
---

## Revision.author property

Gets or sets the author of this revision. Can not be empty string or ``None``.



```python
@property
def author(self) -> str:
    ...

@author.setter
def author(self, value: str):
    ...

```

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # La normale modifica del documento non conta come revisione.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Per registrare le nostre modifiche come revisioni, dobbiamo dichiarare un autore e poi iniziare a tracciarle.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Questa flag corrisponde all'opzione "Review" -> "Tracking" -> "Track Changes" in Microsoft Word.
        # Il metodo "StartTrackRevisions" non influisce sul suo valore,
        # e il documento sta tracciando le revisioni programmaticamente nonostante abbia un valore "false".
        # Se apriamo questo documento con Microsoft Word, non traccerà le revisioni.
        self.assertFalse(doc.track_revisions)
        # Abbiamo aggiunto testo usando il document builder, quindi la prima revisione è una revisione di tipo inserimento.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Rimuovi un run per creare una revisione di tipo eliminazione.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Aggiungere una nuova revisione la posiziona all'inizio della collezione delle revisioni.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Le revisioni di inserimento compaiono nel corpo del documento anche prima di accettare/rifiutare la revisione.
        # Rifiutare la revisione rimuoverà i suoi nodi dal corpo. Al contrario, i nodi che compongono le revisioni di eliminazione
        # rimangono comunque nel documento finché non accettiamo la revisione.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Accettare la revisione di eliminazione rimuoverà il nodo genitore dal testo del paragrafo
        # e quindi rimuoverà la revisione della collezione stessa.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Ora sposta il nodo per creare un tipo di revisione di spostamento.
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
        # La revisione di spostamento è ora all'indice 1. Rifiuta la revisione per scartare il suo contenuto.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

