---
title: DocumentBuilder.is_at_end_of_paragraph property
linktitle: is_at_end_of_paragraph property
articleTitle: is_at_end_of_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_paragraph property. Returns ``True`` if the cursor is at the end of the current paragraph."
type: docs
weight: 110
url: /it/python-net/aspose.words/documentbuilder/is_at_end_of_paragraph/
---

## DocumentBuilder.is_at_end_of_paragraph property

Returns ``True`` if the cursor is at the end of the current paragraph.



```python
@property
def is_at_end_of_paragraph(self) -> bool:
    ...

```

### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un segnalibro valido, un'entità che consiste di nodi racchiusi da un nodo di inizio segnalibro,
# e da un nodo di fine segnalibro.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Il cursore del costruttore di documenti è sempre davanti al nodo che abbiamo aggiunto per ultimo.
# Se il cursore del costruttore è alla fine del documento, il suo nodo corrente sarà nullo.
# Il nodo precedente è il nodo di fine segnalibro che abbiamo aggiunto per ultimo.
# Aggiungere nuovi nodi con il costruttore li aggiungerà al nodo finale.
self.assertIsNone(builder.current_node)
# Se desideriamo modificare una parte diversa del documento con il costruttore,
# dovremo spostare il suo cursore sul nodo che vogliamo modificare.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Spostarlo su un segnalibro lo porterà al primo nodo compreso tra i nodi di inizio e fine segnalibro, il run racchiuso.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Possiamo anche spostare il cursore su un nodo individuale in questo modo.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Possiamo usare metodi specifici per spostarci all'inizio/fine di un documento.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

