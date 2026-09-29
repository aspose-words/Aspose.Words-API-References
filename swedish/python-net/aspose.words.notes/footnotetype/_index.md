---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /sv/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga lite text och markera den med en fotnot med egenskapen IsAuto inställd på "true" som standard,
# så att markören som ses i brödtexten blir automatiskt numrerad till "1",
# och fotnoten kommer att visas längst ner på sidan.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Infoga mer text och markera den med en slutnot med en anpassad referensmarkör,
# som kommer att användas i stället för siffran "2" och sätta "IsAuto" till false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Fotnoter visas alltid längst ner på den refererade texten,
# så att detta sidbrytning inte påverkar fotnoten.
# Å andra sidan är slutnoter alltid i slutet av dokumentet
# så att detta sidbrytning skjuter slutnoten ner till nästa sida.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

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

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

