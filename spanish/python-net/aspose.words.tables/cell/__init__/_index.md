---
title: Cell constructor
linktitle: Cell constructor
articleTitle: Cell constructor
second_title: Aspose.Words for Python
description: "Cell constructor. Initializes a new instance of the [Cell](../) class."
type: docs
weight: 10
url: /es/python-net/aspose.words.tables/cell/__init__/
---

## Cell(doc) {#documentbase}

Initializes a new instance of the [Cell](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Cell](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Cell](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the row where you want the cell inserted.




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
* class [Cell](../)

