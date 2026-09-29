---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /it/python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# Un documento vuoto contiene una sezione per impostazione predefinita,
# che contiene nodi figlio che possiamo modificare.
self.assertEqual(1, doc.sections.count)
# Usa un document builder per aggiungere testo alla prima sezione.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Crea una seconda sezione inserendo un'interruzione di sezione.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Ogni sezione ha le proprie impostazioni di configurazione della pagina.
# Possiamo dividere il testo nella seconda sezione in due colonne.
# Questo non influenzerà il testo nella prima sezione.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

