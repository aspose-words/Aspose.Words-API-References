---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /it/python-net/aspose.words.notes/footnoteoptions/position/
---

## FootnoteOptions.position property

Specifies the footnotes position.


```python
@property
def position(self) -> aspose.words.notes.FootnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.FootnotePosition):
    ...

```

### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

