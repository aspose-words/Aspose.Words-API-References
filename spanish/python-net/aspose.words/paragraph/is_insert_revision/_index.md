---
title: Paragraph.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 110
url: /es/python-net/aspose.words/paragraph/is_insert_revision/
---

## Paragraph.is_insert_revision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```python
@property
def is_insert_revision(self) -> bool:
    ...

```

### Examples

Shows how to work with revision paragraphs.

```python
doc = aw.Document()
body = doc.first_section.body
para = body.first_paragraph
para.append_child(aw.Run(doc=doc, text='Paragraph 1. '))
body.append_paragraph('Paragraph 2. ')
body.append_paragraph('Paragraph 3. ')
# Los párrafos anteriores no son revisiones.
# Los párrafos que añadimos después de iniciar el seguimiento de revisiones se registrarán como revisiones de "Inserción".
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
para = body.append_paragraph('Paragraph 4. ')
self.assertTrue(para.is_insert_revision)
# Los párrafos que eliminamos después de iniciar el seguimiento de revisiones se registrarán como revisiones de "Eliminación".
paragraphs = body.paragraphs
self.assertEqual(4, paragraphs.count)
para = paragraphs[2]
para.remove()
# Estos párrafos permanecerán hasta que aceptemos o rechacemos la revisión de eliminación.
# Aceptar la revisión eliminará el párrafo de forma permanente,
# y rechazar la revisión lo dejará en el documento como si nunca lo hubiéramos eliminado.
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)
# Acepta la revisión y luego verifica que el párrafo haya desaparecido.
doc.accept_all_revisions()
self.assertEqual(3, paragraphs.count)
self.assertEqual(0, para.count)
self.assertEqual('Paragraph 1. \r' + 'Paragraph 2. \r' + 'Paragraph 4.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

