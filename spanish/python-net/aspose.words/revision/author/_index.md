---
title: Revision.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Python
description: "Revision.author property. Gets or sets the author of this revision"
type: docs
weight: 10
url: /es/python-net/aspose.words/revision/author/
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
        # La edición normal del documento no cuenta como una revisión.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Para registrar nuestras ediciones como revisiones, necesitamos declarar un autor y luego comenzar a rastrearlas.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Esta bandera corresponde a la opción "Review" -> "Tracking" -> "Track Changes" en Microsoft Word.
        # El método "StartTrackRevisions" no afecta su valor,
        # y el documento está rastreando revisiones programáticamente a pesar de que tiene un valor de "false".
        # Si abrimos este documento con Microsoft Word, no rastreará revisiones.
        self.assertFalse(doc.track_revisions)
        # Hemos añadido texto usando el generador de documentos, por lo que la primera revisión es una revisión de tipo inserción.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Elimina una ejecución para crear una revisión de tipo eliminación.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Agregar una nueva revisión la coloca al principio de la colección de revisiones.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Las revisiones de inserción aparecen en el cuerpo del documento incluso antes de que aceptemos/rechacemos la revisión.
        # Rechazar la revisión eliminará sus nodos del cuerpo. Por el contrario, los nodos que componen revisiones de eliminación
        # también permanecen en el documento hasta que aceptemos la revisión.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Aceptar la revisión de eliminación eliminará su nodo padre del texto del párrafo
        # y luego eliminará la propia revisión de la colección.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Ahora mueva el nodo para crear un tipo de revisión en movimiento.
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
        # La revisión en movimiento está ahora en el índice 1. Rechace la revisión para descartar su contenido.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

