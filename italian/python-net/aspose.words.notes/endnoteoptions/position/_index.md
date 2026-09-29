---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /it/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una nota finale è un modo per allegare un riferimento o un commento laterale al testo
# che non interferisce con il flusso del testo principale.
# L'inserimento di una nota finale aggiunge un piccolo simbolo di riferimento in apice
# nel testo principale dove inseriamo la nota finale.
# Ogni nota finale crea anche una voce alla fine del documento, composta da un simbolo
# che corrisponde al simbolo di riferimento nel testo principale.
# Il testo di riferimento che passiamo al metodo "InsertEndnote" del document builder.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Possiamo usare la proprietà "Position" per determinare dove il documento posizionerà tutte le sue note finali.
# Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfDocument",
# ogni nota a piè di pagina verrà mostrata in una raccolta alla fine del documento. Questo è il valore predefinito.
# Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfSection",
# ogni nota a piè di pagina verrà visualizzata in una raccolta alla fine della sezione il cui testo contiene il segno di riferimento della nota finale.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

