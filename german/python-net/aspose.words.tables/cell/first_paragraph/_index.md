---
title: Cell.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "Cell.first_paragraph property. Gets the first paragraph among the immediate children."
type: docs
weight: 30
url: /de/python-net/aspose.words.tables/cell/first_paragraph/
---

## Cell.first_paragraph property

Gets the first paragraph among the immediate children.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to create a nested table using a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstelle die äußere Tabelle.
cell = builder.insert_cell()
builder.writeln('Outer Table Cell 1')
builder.insert_cell()
builder.writeln('Outer Table Cell 2')
builder.end_table()
# Gehe zur ersten Zelle der äußeren Tabelle und erstelle eine weitere Tabelle in der Zelle.
builder.move_to(cell.first_paragraph)
builder.insert_cell()
builder.writeln('Inner Table Cell 1')
builder.insert_cell()
builder.writeln('Inner Table Cell 2')
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertNestedTable.docx')
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
* class [Cell](../)

