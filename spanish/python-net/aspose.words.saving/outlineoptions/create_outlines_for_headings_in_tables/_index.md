---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /es/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
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
# Crea una tabla con tres filas. La primera fila,
# cuyo texto formatearemos en un estilo tipo encabezado, servirá como encabezado de columna.
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
# Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su encabezado correspondiente.
# Establece la propiedad "HeadingsOutlineLevels" a "1" para obtener el esquema
# para registrar solo encabezados con niveles de encabezado que no sean mayores que 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# Establece la propiedad "CreateOutlinesForHeadingsInTables" a "false" para excluir todos los encabezados dentro de tablas,
# como la que hemos creado arriba del esquema.
# Establece la propiedad "CreateOutlinesForHeadingsInTables" a "true" para incluir todos los encabezados dentro de tablas
# en el esquema, siempre que tengan un nivel de encabezado que no sea mayor que el valor de la propiedad "HeadingsOutlineLevels".
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

