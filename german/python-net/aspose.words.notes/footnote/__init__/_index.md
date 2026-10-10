---
title: Footnote constructor
linktitle: Footnote constructor
articleTitle: Footnote constructor
second_title: Aspose.Words for Python
description: "Footnote constructor. Initializes an instance of the [Footnote](../) class."
type: docs
weight: 10
url: /de/python-net/aspose.words.notes/footnote/__init__/
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
# Fügen Sie Text hinzu und verweisen Sie darauf mit einer Fußnote. Diese Fußnote wird ein kleines hochgestelltes Referenzzeichen setzen
# nach dem Text, auf den sie verweist, und einen Eintrag unterhalb des Haupttextes am unteren Rand der Seite erzeugen.
# Dieser Eintrag wird das Referenzzeichen der Fußnote und den Referenztext enthalten,
# das wir an die "InsertFootnote"-Methode des Dokumenten‑Builders übergeben werden.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
# ihr Index unter allen Fußnoten des Abschnitts.
# Dies ist die erste Fußnote, also wird das Referenzzeichen "1" sein.
self.assertTrue(footnote.is_auto)
# Wir können den Dokumenten‑Builder in die Fußnote verschieben, um deren Referenztext zu bearbeiten.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Ein Lesezeichen mit dem "IsAuto"-Flag, das auf true gesetzt ist, zeigt weiterhin seinen echten Index
# selbst wenn vorherige Lesezeichen benutzerdefinierte Referenzmarken anzeigen, wird die Referenzmarke dieses Lesezeichens eine "3" sein.
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

