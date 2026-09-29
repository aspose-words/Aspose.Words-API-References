---
title: Paragraph constructor
linktitle: Paragraph constructor
articleTitle: Paragraph constructor
second_title: Aspose.Words for Python
description: "Paragraph constructor. Initializes a new instance of the [Paragraph](../) class."
type: docs
weight: 10
url: /it/python-net/aspose.words/paragraph/__init__/
---

## Paragraph(doc) {#documentbase}

Initializes a new instance of the [Paragraph](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Paragraph](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Paragraph](../) to the document use [CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
on the story where you want the paragraph inserted.




### Examples

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
* class [Paragraph](../)

