---
title: Table.allow_cell_spacing property
linktitle: allow_cell_spacing property
articleTitle: allow_cell_spacing property
second_title: Aspose.Words for Python
description: "Table.allow_cell_spacing property. Gets or sets the Allow spacing between cells option."
type: docs
weight: 60
url: /it/python-net/aspose.words.tables/table/allow_cell_spacing/
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
# Imposta la proprietà "AllowCellSpacing" su "true" per abilitare la spaziatura tra le celle
# con un valore pari a quello della proprietà "CellSpacing", in punti.
# Imposta la proprietà "AllowCellSpacing" su "false" per disabilitare la spaziatura tra le celle
# e ignora il valore della proprietà "CellSpacing".
table.allow_cell_spacing = allow_cell_spacing
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowCellSpacing.html')
# Regolare la proprietà "CellSpacing" abiliterà automaticamente la spaziatura tra le celle.
table.cell_spacing = 5
self.assertTrue(table.allow_cell_spacing)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

