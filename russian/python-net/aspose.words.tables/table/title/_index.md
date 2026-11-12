---
title: Table.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Table.title property. Gets or sets title of this table"
type: docs
weight: 320
url: /ru/python-net/aspose.words.tables/table/title/
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

