---
title: Table constructor
linktitle: Table constructor
articleTitle: Table constructor
second_title: Aspose.Words for Python
description: "Table constructor. Initializes a new instance of the [Table](../) class."
type: docs
weight: 10
url: /de/python-net/aspose.words.tables/table/__init__/
---

## Table(doc) {#documentbase}

Initializes a new instance of the [Table](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Table](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Table](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the story where you want the table inserted.




### Examples

Shows how to create a table.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
# Tabellen enthalten Zeilen, die Zellen enthalten, die wiederum Absätze haben können
# mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
# Der Aufruf der "EnsureMinimum"-Methode auf einer Tabelle stellt sicher, dass
# die Tabelle mindestens eine Zeile, Zelle und Absatz enthält.
first_row = aw.tables.Row(doc)
table.append_child(first_row)
first_cell = aw.tables.Cell(doc)
first_row.append_child(first_cell)
paragraph = aw.Paragraph(doc)
first_cell.append_child(paragraph)
# Fügen Sie Text zur ersten Zelle in der ersten Zeile der Tabelle hinzu.
run = aw.Run(doc=doc, text='Hello world!')
paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateTable.docx')
```

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# Erstellen Sie die äußere Tabelle mit drei Zeilen und vier Spalten und fügen Sie sie anschließend dem Dokument hinzu.
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# Erstellen Sie eine weitere Tabelle mit zwei Zeilen und zwei Spalten und fügen Sie sie dann in die erste Zelle der ersten Tabelle ein.
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
    # Sie können die Eigenschaften "Title" und "Description" verwenden, um Ihrer Tabelle jeweils einen Titel und eine Beschreibung hinzuzufügen.
    # Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    # Diese Eigenschaften sind für ISO/IEC‑29500‑konforme .docx‑Dokumente sinnvoll (siehe die Klasse OoxmlCompliance).
    # Wenn wir das Dokument in Formate vor ISO/IEC 29500 speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

