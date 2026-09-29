---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /it/python-net/aspose.words.notes/footnote/reference_mark/
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

* module [aspose.words.notes](../../)
* class [Footnote](../)

