---
title: Node.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Node.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /it/python-net/aspose.words/node/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci paragrafi con testo usando DocumentBuilder.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Convertire il documento in forma testuale rivela che i caratteri di controllo
# rappresentano alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# Durante la conversione di un documento in forma stringa,
# possiamo omettere alcuni dei caratteri di controllo con il metodo Trim.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
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
* class [Node](../)

