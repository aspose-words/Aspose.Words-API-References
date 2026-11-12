---
title: Table constructor
linktitle: Table constructor
articleTitle: Table constructor
second_title: Aspose.Words for Python
description: "Table constructor. Initializes a new instance of the [Table](../) class."
type: docs
weight: 10
url: /ru/python-net/aspose.words.tables/table/__init__/
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
# Таблицы содержат строки, которые содержат ячейки, которые могут иметь абзацы
# с типичными элементами, такими как текстовые фрагменты, фигуры и даже другие таблицы.
# Вызов метода "EnsureMinimum" у таблицы гарантирует, что
# у таблицы будет как минимум одна строка, ячейка и абзац.
first_row = aw.tables.Row(doc)
table.append_child(first_row)
first_cell = aw.tables.Cell(doc)
first_row.append_child(first_cell)
paragraph = aw.Paragraph(doc)
first_cell.append_child(paragraph)
# Добавьте текст в первую ячейку первой строки таблицы.
run = aw.Run(doc=doc, text='Hello world!')
paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateTable.docx')
```

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# Создайте внешнюю таблицу с тремя строками и четырьмя столбцами, а затем добавьте её в документ.
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# Создайте другую таблицу с двумя строками и двумя столбцами и вставьте её в первую ячейку первой таблицы.
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
    # Вы можете использовать свойства "Title" и "Description", чтобы соответственно добавить заголовок и описание к вашей таблице.
    # Таблица должна иметь как минимум одну строку, прежде чем мы сможем использовать эти свойства.
    # Эти свойства имеют смысл для .docx‑документов, соответствующих ISO / IEC 29500 (см. класс OoxmlCompliance).
    # Если мы сохраняем документ в форматы до ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

