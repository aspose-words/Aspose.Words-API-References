---
title: Footnote constructor
linktitle: Footnote constructor
articleTitle: Footnote constructor
second_title: Aspose.Words for Python
description: "Footnote constructor. Initializes an instance of the [Footnote](../) class."
type: docs
weight: 10
url: /sv/python-net/aspose.words.notes/footnote/__init__/
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
# Lägg till text och referera den med en fotnot. Denna fotnot kommer att placera en liten upphöjd referens
# markering efter texten som den refererar till och skapa en post under huvudtexten längst ner på sidan.
# Denna post kommer att innehålla fotnotens referensmarkör och referenstexten,
# som vi kommer att skicka till dokumentbyggarens "InsertFootnote"-metod.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Om denna egenskap är inställd på "true", så blir vår fotnotens referensmarkör
# dess index bland alla sektionens fotnoter.
# Detta är den första fotnoten, så referensmarkören blir "1".
self.assertTrue(footnote.is_auto)
# Vi kan flytta dokumentbyggaren inuti fotnoten för att redigera dess referenstext.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Vi kan ange en anpassad referensmarkör som fotnoten kommer att använda i stället för sitt indexnummer.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Ett bokmärke med flaggan "IsAuto" inställd på true kommer fortfarande att visa sitt verkliga index
# även om tidigare bokmärken visar anpassade referensmarkeringar, så kommer detta bokmärkes referensmarkering att vara en "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

