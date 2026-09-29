---
title: FootnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "FootnoteOptions.number_style property. Specifies the number format for automatically numbered footnotes."
type: docs
weight: 20
url: /it/python-net/aspose.words.notes/footnoteoptions/number_style/
---

## FootnoteOptions.number_style property

Specifies the number format for automatically numbered footnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

