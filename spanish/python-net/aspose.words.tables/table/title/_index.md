---
title: Table.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Table.title property. Gets or sets title of this table"
type: docs
weight: 320
url: /es/python-net/aspose.words.tables/table/title/
---

## Table.title property

Gets or sets title of this table.
It provides an alternative text representation of the information contained in the table.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents
([OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)).
When saved to pre-ISO/IEC 29500 formats, the property is ignored.




### Examples

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# Cree la tabla externa con tres filas y cuatro columnas, y luego agréguela al documento.
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# Cree otra tabla con dos filas y dos columnas y luego insértela en la primera celda de la primera tabla.
inner_table = ExTable._create_table(doc, 2, 2, 'Inner Table')
outer_table.first_row.first_cell.append_child(inner_table)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateNestedTable.docx')
```

Shows how to build a nested table without using a document builder (CreateTable).

```python
@staticmethod
def _create_table(doc, row_count, cell_count, cell_text):
    table = aw.tables.Table(doc)
    row_id = 1
    while row_id <= row_count:
        row = aw.tables.Row(doc)
        table.append_child(row)
        cell_id = 1
        while cell_id <= cell_count:
            cell = aw.tables.Cell(doc)
            cell.append_child(aw.Paragraph(doc))
            cell.first_paragraph.append_child(aw.Run(doc=doc, text=cell_text))
            row.append_child(cell)
            cell_id += 1
        row_id += 1
    # Puede usar las propiedades "Title" y "Description" para agregar un título y una descripción respectivamente a su tabla.
    # La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    # Estas propiedades son relevantes para documentos .docx compatibles con ISO / IEC 29500 (vea la clase OoxmlCompliance).
    # Si guardamos el documento en formatos pre-ISO/IEC 2950, Microsoft Word ignora estas propiedades.
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

