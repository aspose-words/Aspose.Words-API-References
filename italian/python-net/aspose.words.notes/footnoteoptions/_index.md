---
title: FootnoteOptions class
linktitle: FootnoteOptions class
articleTitle: FootnoteOptions class
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteOptions class. Represents the footnote numbering options for a document or section"
type: docs
weight: 50
url: /it/python-net/aspose.words.notes/footnoteoptions/
---

## FootnoteOptions class

Represents the footnote numbering options for a document or section.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/python-net/working-with-footnote-and-endnote/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [columns](./columns/) | Specifies the number of columns with which the footnotes area is formatted. |
| [number_style](./number_style/) | Specifies the number format for automatically numbered footnotes. |
| [position](./position/) | Specifies the footnotes position. |
| [restart_rule](./restart_rule/) | Determines when automatic numbering restarts. |
| [start_number](./start_number/) | Specifies the starting number or character for the first automatically numbered footnotes. |

### Examples

Shows how to split the footnote section into a given number of columns.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
doc.footnote_options.columns = 2
doc.save(file_name=ARTIFACTS_DIR + 'Document.FootnoteColumns.docx')
```

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una nota a piè di pagina è un modo per allegare un riferimento o un commento laterale al testo
# che non interferisce con il flusso del testo principale.
# L'inserimento di una nota a piè di pagina aggiunge un piccolo simbolo di riferimento in apice
# nel testo principale dove inseriamo la nota a piè di pagina.
# Ogni nota a piè di pagina crea anche una voce nella parte inferiore della pagina, costituita da un simbolo
# che corrisponde al simbolo di riferimento nel testo principale.
# Il testo di riferimento che passiamo al metodo "InsertFootnote" del costruttore di documenti.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Possiamo usare la proprietà "Position" per determinare dove il documento posizionerà tutte le sue note a piè di pagina.
# Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BottomOfPage",
# ogni nota a piè di pagina verrà visualizzata nella parte inferiore della pagina che contiene il suo segno di riferimento. Questo è il valore predefinito.
# Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BeneathText",
# ogni nota a piè di pagina verrà visualizzata alla fine del testo della pagina che contiene il suo segno di riferimento.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

Shows how to change the number style of footnote/endnote reference marks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
# che non interferisce con il flusso del testo principale.
# L'inserimento di una nota a piè di pagina/note finale aggiunge un piccolo simbolo di riferimento in apice
# nel testo principale dove inseriamo la nota a piè di pagina/note finale.
# Ogni nota a piè di pagina/note finale crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
# simbolo nel testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del costruttore di documenti.
# Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate nella parte inferiore di ogni pagina che contiene
# i loro simboli di riferimento, e le note finali vengono visualizzate alla fine del documento.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota finale è il suo indice
# tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
# per le note a piè di pagina e per le note finali. Per impostazione predefinita, le note a piè di pagina mostrano i loro numeri usando numeri arabi,
# e le note finali mostrano i loro numeri in numeri romani minuscoli.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Possiamo usare la proprietà "NumberStyle" per applicare stili di numerazione personalizzati a note a piè di pagina e note finali.
# Questo non influenzerà le note a piè di pagina/note finali con segni di riferimento personalizzati.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
# che non interferisce con il flusso del testo principale.
# L'inserimento di una nota a piè di pagina/note finale aggiunge un piccolo simbolo di riferimento in apice
# nel testo principale dove inseriamo la nota a piè di pagina/note finale.
# Ogni nota a piè di pagina/note finale crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
# simbolo nel testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del costruttore di documenti.
# Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate nella parte inferiore di ogni pagina che contiene
# i loro simboli di riferimento, e le note finali vengono visualizzate alla fine del documento.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota finale è il suo indice
# tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
# per le note a piè di pagina e le note finali e non riavvia questi conteggi in nessun momento.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Possiamo usare la proprietà "RestartRule" per far ripartire il documento
# il conteggio delle note a piè di pagina/note di chiusura avviene in una nuova pagina o sezione.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
# che non interferisce con il flusso del testo principale.
# L'inserimento di una nota a piè di pagina/note finale aggiunge un piccolo simbolo di riferimento in apice
# nel testo principale dove inseriamo la nota a piè di pagina/note finale.
# Ogni nota a piè di pagina/note di chiusura crea anche una voce, che consiste in un simbolo
# che corrisponde al simbolo di riferimento nel testo principale.
# Il testo di riferimento che passiamo al metodo "InsertEndnote" del document builder.
# Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate nella parte inferiore di ogni pagina che contiene
# i loro simboli di riferimento, e le note finali vengono visualizzate alla fine del documento.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota finale è il suo indice
# tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
# per le note a piè di pagina e per le note di chiusura, che entrambe iniziano da 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Possiamo usare la proprietà "StartNumber" per far sì che il documento
# inizii il conteggio di una nota a piè di pagina o di una nota di chiusura con un numero diverso.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../)
* property [Document.footnote_options](../../aspose.words/document/footnote_options/)
* property [PageSetup.footnote_options](../../aspose.words/pagesetup/footnote_options/)

