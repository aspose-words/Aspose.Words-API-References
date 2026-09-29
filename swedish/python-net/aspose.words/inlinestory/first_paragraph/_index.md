---
title: InlineStory.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.first_paragraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /sv/python-net/aspose.words/inlinestory/first_paragraph/
---

## InlineStory.first_paragraph property

Gets the first paragraph in the story.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

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

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# I Microsoft Word kan vi högerklicka på den här kommentaren i dokumentets body för att redigera den, eller svara på den.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

