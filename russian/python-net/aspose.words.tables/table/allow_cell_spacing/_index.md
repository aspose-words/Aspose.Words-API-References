---
title: Table.allow_cell_spacing property
linktitle: allow_cell_spacing property
articleTitle: allow_cell_spacing property
second_title: Aspose.Words for Python
description: "Table.allow_cell_spacing property. Gets or sets the Allow spacing between cells option."
type: docs
weight: 60
url: /ru/python-net/aspose.words.tables/table/allow_cell_spacing/
---

## Table.allow_cell_spacing property

Gets or sets the "Allow spacing between cells" option.


```python
@property
def allow_cell_spacing(self) -> bool:
    ...

@allow_cell_spacing.setter
def allow_cell_spacing(self, value: bool):
    ...

```

### Examples

Shows how to enable spacing between individual cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Animal')
builder.insert_cell()
builder.write('Class')
builder.end_row()
builder.insert_cell()
builder.write('Dog')
builder.insert_cell()
builder.write('Mammal')
builder.end_table()
table.cell_spacing = 3
# Установите свойство "AllowCellSpacing" в значение "true", чтобы включить интервал между ячейками
# с величиной, равной значению свойства "CellSpacing", в пунктах.
# Установите свойство "AllowCellSpacing" в значение "false", чтобы отключить интервал между ячейками
# и игнорировать значение свойства "CellSpacing".
table.allow_cell_spacing = allow_cell_spacing
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowCellSpacing.html')
# Изменение свойства "CellSpacing" автоматически включит интервал между ячейками.
table.cell_spacing = 5
self.assertTrue(table.allow_cell_spacing)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

