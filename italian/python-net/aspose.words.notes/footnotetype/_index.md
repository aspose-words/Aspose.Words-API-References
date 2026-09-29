---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /it/python-net/aspose.words.notes/footnotetype/
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
# Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
# in modo che il marcatore visualizzato nel testo principale sia numerato automaticamente a "1",
# e la nota a piè di pagina apparirà in fondo alla pagina.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Inserisci altro testo e contrassegnalo con una nota di chiusura con un marcatore di riferimento personalizzato,
# che verrà usato al posto del numero "2" e imposterà "IsAuto" su false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Le note a piè di pagina appaiono sempre in fondo al loro testo di riferimento,
# quindi questo interruzione di pagina non influenzerà la nota a piè di pagina.
# D'altra parte, le note di chiusura sono sempre alla fine del documento
# in modo che questa interruzione di pagina spinga la nota di chiusura alla pagina successiva.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aggiungi testo e riferiscilo con una nota a piè di pagina. Questa nota a piè di pagina inserirà un piccolo riferimento in apice
# dopo il testo a cui fa riferimento e creerà una voce sotto il testo principale in fondo alla pagina.
# Questa voce conterrà il marcatore di riferimento della nota a piè di pagina e il testo di riferimento,
# che passeremo al metodo "InsertFootnote" del costruttore di documenti.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Se questa proprietà è impostata su "true", allora il marcatore di riferimento della nostra nota a piè di pagina
# sarà il suo indice tra tutte le note a piè di pagina della sezione.
# Questa è la prima nota a piè di pagina, quindi il marcatore di riferimento sarà "1".
self.assertTrue(footnote.is_auto)
# Possiamo spostare il costruttore di documenti all'interno della nota a piè di pagina per modificare il suo testo di riferimento.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Possiamo impostare un marcatore di riferimento personalizzato che la nota a piè di pagina utilizzerà al posto del suo numero di indice.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Un segnalibro con l'opzione \"IsAuto\" impostata su true mostrerà comunque il suo indice reale
# anche se i segnalibri precedenti mostrano segni di riferimento personalizzati, quindi il segno di riferimento di questo segnalibro sarà un \"3\".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

