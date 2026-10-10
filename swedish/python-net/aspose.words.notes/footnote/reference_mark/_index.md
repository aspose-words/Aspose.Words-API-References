---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /sv/python-net/aspose.words.notes/footnote/reference_mark/
---

## Footnote.reference_mark property

Gets/sets custom reference mark to be used for this footnote.
Default value is **empty string** (), meaning auto-numbered footnotes are used.



```python
@property
def reference_mark(self) -> str:
    ...

@reference_mark.setter
def reference_mark(self, value: str):
    ...

```

### Remarks

If this property is set to **empty string** () or ``None``, then [Footnote.is_auto](../is_auto/) property will automatically be set to ``True``, 
if set to anything else then [Footnote.is_auto](../is_auto/) will be set to ``False``.


RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.




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

