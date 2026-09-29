---
title: ParagraphFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "ParagraphFormat.alignment property. Gets or sets text alignment for the paragraph."
type: docs
weight: 30
url: /it/python-net/aspose.words/paragraphformat/alignment/
---

## ParagraphFormat.alignment property

Gets or sets text alignment for the paragraph.


```python
@property
def alignment(self) -> aspose.words.ParagraphAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.ParagraphAlignment):
    ...

```

### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Arial'
font.underline = aw.Underline.DASH
paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True
# Il metodo \"Writeln\" termina il paragrafo dopo aver aggiunto il testo
# e poi avvia una nuova riga, aggiungendo un nuovo paragrafo.
builder.writeln('Hello world!')
self.assertTrue(builder.current_paragraph.is_end_of_document)
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Un documento vuoto contiene una sezione, un corpo e un paragrafo.
# Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
# e otterrai un nodo documento senza figli.
doc.remove_all_children()
# Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuto.
# Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
# Prima, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
section = aw.Section(doc)
doc.append_child(section)
# Imposta alcune proprietà di configurazione della pagina per la sezione.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
# sulla pagina tra l'intestazione e il piè di pagina della sezione.
body = aw.Body(doc)
section.append_child(body)
# Crea un paragrafo, imposta alcune proprietà di formattazione, quindi aggiungilo come figlio al corpo.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Infine, aggiungi del contenuto al documento. Crea una run,
# imposta il suo aspetto e i suoi contenuti, quindi aggiungila come figlio al paragrafo.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

