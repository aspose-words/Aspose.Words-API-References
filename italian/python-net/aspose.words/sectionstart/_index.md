---
title: SectionStart enumeration
linktitle: SectionStart enumeration
articleTitle: SectionStart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.SectionStart enumeration. The type of break at the beginning of the section."
type: docs
weight: 1170
url: /it/python-net/aspose.words/sectionstart/
---

## SectionStart enumeration

The type of break at the beginning of the section.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | The new section starts on the same page as the previous section. |
| NEW_COLUMN | The section starts from a new column. |
| NEW_PAGE | The section starts from a new page. |
| EVEN_PAGE | The section starts on a new even page. |
| ODD_PAGE | The section starts on a new odd page. |

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# I tipi di interruzione di sezione determinano come una nuova sezione si separa dalla sezione precedente.
# Di seguito sono riportati cinque tipi di interruzioni di sezione.
# 1 -  Avvia la sezione successiva su una nuova pagina:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  Avvia la sezione successiva nella pagina corrente:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  Avvia la sezione successiva su una nuova pagina pari:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  Avvia la sezione successiva su una nuova pagina dispari:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  Avvia la sezione successiva su una nuova colonna:
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
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

* module [aspose.words](../)

