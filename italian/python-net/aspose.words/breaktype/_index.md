---
title: BreakType enumeration
linktitle: BreakType enumeration
articleTitle: BreakType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.BreakType enumeration. Specifies type of a break inside a document."
type: docs
weight: 120
url: /it/python-net/aspose.words/breaktype/
---

## BreakType enumeration

Specifies type of a break inside a document.


### Members

| Name | Description |
| --- | --- |
| PARAGRAPH_BREAK | Break between paragraphs. |
| PAGE_BREAK | Explicit page break. |
| COLUMN_BREAK | Explicit column break. |
| SECTION_BREAK_CONTINUOUS | Specifies start of new section on the same page as the previous section. |
| SECTION_BREAK_NEW_COLUMN | Specifies start of new section in the new column. |
| SECTION_BREAK_NEW_PAGE | Specifies start of new section on a new page. |
| SECTION_BREAK_EVEN_PAGE | Specifies start of new section on a new even page. |
| SECTION_BREAK_ODD_PAGE | Specifies start of new section on a odd page. |
| LINE_BREAK | Explicit line break. |

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Specifica che vogliamo intestazioni e piè di pagina diversi per la prima, le pagine pari e dispari.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Crea le intestazioni, poi aggiungi tre pagine al documento per visualizzare ogni tipo di intestazione.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un indice per la prima pagina del documento.
# Configura la tabella per includere i paragrafi con intestazioni di livello da 1 a 3.
# Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
# alla posizione dell'intestazione quando si fa clic sinistro in Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Popola l'indice aggiungendo paragrafi con stili di intestazione.
# Ogni intestazione di questo tipo con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifica le proprietà di impostazione pagina per la sezione corrente del builder e aggiungi testo.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Se avviamo una nuova sezione utilizzando un document builder,
# eredità le proprietà di impostazione pagina correnti del builder.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Possiamo ripristinare le sue proprietà di impostazione pagina ai valori predefiniti usando il metodo "ClearFormatting".
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)

