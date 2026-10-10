---
title: Footnote.is_auto property
linktitle: is_auto property
articleTitle: is_auto property
second_title: Aspose.Words for Python
description: "Footnote.is_auto property. Holds a value that specifies whether this is a auto-numbered footnote or  footnote with user defined custom reference mark."
type: docs
weight: 40
url: /it/python-net/aspose.words.notes/footnote/is_auto/
---

## Footnote.is_auto property

Holds a value that specifies whether this is a auto-numbered footnote or 
footnote with user defined custom reference mark.


```python
@property
def is_auto(self) -> bool:
    ...

@is_auto.setter
def is_auto(self, value: bool):
    ...

```

### Remarks

[Footnote.reference_mark](../reference_mark/) initialized with empty string if [Footnote.is_auto](./) set to ``False``.



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

