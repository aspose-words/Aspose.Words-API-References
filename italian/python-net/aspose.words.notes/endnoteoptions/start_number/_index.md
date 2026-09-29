---
title: EndnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "EndnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered endnotes."
type: docs
weight: 40
url: /it/python-net/aspose.words.notes/endnoteoptions/start_number/
---

## EndnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered endnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [EndnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

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

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

