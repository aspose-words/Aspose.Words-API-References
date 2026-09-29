---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /it/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Il costruttore di documenti ha un cursore, che funge da parte del documento
# dove il costruttore aggiunge nuovi nodi quando utilizziamo i suoi metodi di costruzione del documento.
# Questo cursore funziona allo stesso modo del cursore lampeggiante di Microsoft Word,
# e finisce sempre immediatamente dopo qualsiasi nodo che il costruttore ha appena inserito.
# Per aggiungere contenuto a una parte diversa del documento,
# possiamo spostare il cursore su un nodo diverso con il metodo "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Il cursore è ora davanti al nodo a cui lo abbiamo spostato.
# Aggiungere una seconda sequenza la inserirà davanti alla prima sequenza.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Sposta il cursore alla fine del documento per continuare ad aggiungere testo alla fine come prima.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

