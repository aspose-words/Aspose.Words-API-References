---
title: Footnote constructor
linktitle: Footnote constructor
articleTitle: Footnote constructor
second_title: Aspose.Words for Python
description: "Footnote constructor. Initializes an instance of the [Footnote](../) class."
type: docs
weight: 10
url: /es/python-net/aspose.words.notes/footnote/__init__/
---

## Footnote(doc, footnote_type) {#documentbase_footnotetype}

Initializes an instance of the [Footnote](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase, footnote_type: aspose.words.notes.FootnoteType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| footnote_type | [FootnoteType](../../footnotetype/) | A [Footnote.footnote_type](../footnote_type/) value that specifies whether this is a footnote or endnote. |

### Remarks

When [Footnote](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Footnote](../) to the document use[CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the paragraph where you want the footnote inserted.




### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregue texto y refiérencielo con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice
# después del texto al que hace referencia y creará una entrada debajo del texto principal al final de la página.
# Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
# que pasaremos al método "InsertFootnote" del generador de documentos.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Si esta propiedad se establece en "true", entonces la marca de referencia de nuestra nota al pie
# será su índice entre todas las notas al pie de la sección.
# Esta es la primera nota al pie, por lo que la marca de referencia será "1".
self.assertTrue(footnote.is_auto)
# Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Podemos establecer una marca de referencia personalizada que la nota al pie usará en lugar de su número de índice.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Un marcador con la bandera "IsAuto" establecida en true aún mostrará su índice real
# incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

