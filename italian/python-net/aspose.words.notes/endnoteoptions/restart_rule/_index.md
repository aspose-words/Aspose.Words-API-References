---
title: EndnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "EndnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 30
url: /it/python-net/aspose.words.notes/endnoteoptions/restart_rule/
---

## EndnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Remarks

Not all values are applicable to endnotes.
To ascertain which values are applicable see [FootnoteNumberingRule](../../footnotenumberingrule/).




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

