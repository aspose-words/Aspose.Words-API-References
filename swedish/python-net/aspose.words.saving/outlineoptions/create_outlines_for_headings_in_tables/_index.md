---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /sv/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
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
# Skapa en tabell med tre rader. Den första raden,
# vars text vi kommer att formatera i en rubrikliknande stil, kommer att fungera som kolumnrubrik.
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Den resulterande PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
# Att klicka på en post i denna disposition tar oss till platsen för dess respektive rubrik.
# Ställ in egenskapen \"HeadingsOutlineLevels\" till \"1\" för att få dispositionen
# för att endast registrera rubriker med rubriknivåer som inte är större än 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# Ställ in egenskapen \"CreateOutlinesForHeadingsInTables\" till \"false\" för att utesluta alla rubriker i tabeller,
# såsom den vi skapade ovan från dispositionen.
# Ställ in egenskapen \"CreateOutlinesForHeadingsInTables\" till \"true\" för att inkludera alla rubriker i tabeller
# i dispositionen, förutsatt att de har en rubriknivå som inte är större än värdet på egenskapen \"HeadingsOutlineLevels\".
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

