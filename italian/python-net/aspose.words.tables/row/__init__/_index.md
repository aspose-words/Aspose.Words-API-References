---
title: Row constructor
linktitle: Row constructor
articleTitle: Row constructor
second_title: Aspose.Words for Python
description: "Row constructor. Initializes a new instance of the [Row](../) class."
type: docs
weight: 10
url: /it/python-net/aspose.words.tables/row/__init__/
---

## Row(doc) {#documentbase}

Initializes a new instance of the [Row](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Row](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Row](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the table where you want the row inserted.




### Examples

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# Crea la tabella esterna con tre righe e quattro colonne, quindi aggiungila al documento.
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# Crea un'altra tabella con due righe e due colonne e poi inseriscila nella prima cella della prima tabella.
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
    # Puoi usare le proprietà "Title" e "Description" per aggiungere rispettivamente un titolo e una descrizione alla tua tabella.
    # La tabella deve avere almeno una riga prima di poter usare queste proprietà.
    # Queste proprietà sono significative per i documenti .docx conformi a ISO / IEC 29500 (vedi la classe OoxmlCompliance).
    # Se salviamo il documento in formati pre-ISO/IEC 29500, Microsoft Word ignora queste proprietà.
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

