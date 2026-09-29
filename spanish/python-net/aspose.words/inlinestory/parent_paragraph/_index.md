---
title: InlineStory.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.parent_paragraph property. Retrieves the parent [Paragraph](../../paragraph/) of this node."
type: docs
weight: 90
url: /es/python-net/aspose.words/inlinestory/parent_paragraph/
---

## InlineStory.parent_paragraph property

Retrieves the parent [Paragraph](../../paragraph/) of this node.



```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# Los nodos de tabla tienen un método "EnsureMinimum()" que asegura que la tabla tenga al menos una celda.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Podemos colocar una tabla dentro de una nota al pie, lo que hará que aparezca en el pie de página de la página de referencia.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# Un InlineStory también tiene un método "EnsureMinimum()", pero en este caso,
# asegura que el último hijo del nodo sea un párrafo,
# para que podamos hacer clic y escribir texto fácilmente en Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Edite la apariencia del ancla, que es el pequeño número en superíndice
# en el texto principal que apunta a la nota al pie.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Todos los nodos de historia en línea tienen sus respectivos tipos de historia.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Un comentario es otro tipo de historia en línea.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# El párrafo padre de un nodo de historia en línea será el del cuerpo principal del documento.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Sin embargo, el último párrafo es el del contenido de texto del comentario,
# que estará fuera del cuerpo principal del documento en una burbuja de discurso.
# Un comentario no tendrá nodos hijos por defecto,
# por lo que podemos aplicar el método EnsureMinimum() para colocar un párrafo aquí también.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Una vez que tengamos un párrafo, podemos mover el constructor para hacerlo y escribir nuestro comentario.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

