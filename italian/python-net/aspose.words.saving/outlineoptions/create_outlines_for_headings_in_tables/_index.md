---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /it/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea una tabella con tre righe. La prima riga,
# il cui testo formatteremo in uno stile tipo intestazione, servirà come intestazione di colonna.
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Il documento PDF di output conterrà un sommario, che è una tabella dei contenuti che elenca le intestazioni nel corpo del documento.
# Fare clic su una voce di questa struttura ci porterà alla posizione della relativa intestazione.
# Imposta la proprietà "HeadingsOutlineLevels" su "1" per ottenere la struttura
# per registrare solo le intestazioni con livelli di intestazione non superiori a 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "false" per escludere tutte le intestazioni all'interno delle tabelle,
# come quella che abbiamo creato sopra dalla struttura.
# Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "true" per includere tutte le intestazioni all'interno delle tabelle
# nella struttura, a condizione che abbiano un livello di intestazione non superiore al valore della proprietà "HeadingsOutlineLevels".
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

