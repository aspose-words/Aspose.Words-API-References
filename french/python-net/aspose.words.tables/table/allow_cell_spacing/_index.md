---
title: Table.allow_cell_spacing property
linktitle: allow_cell_spacing property
articleTitle: allow_cell_spacing property
second_title: Aspose.Words for Python
description: "Table.allow_cell_spacing property. Gets or sets the Allow spacing between cells option."
type: docs
weight: 60
url: /fr/python-net/aspose.words.tables/table/allow_cell_spacing/
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
# Définissez la propriété "AllowCellSpacing" sur "true" pour activer l'espacement entre les cellules
# avec une magnitude égale à la valeur de la propriété "CellSpacing", en points.
# Définissez la propriété "AllowCellSpacing" sur "false" pour désactiver l'espacement des cellules
# et ignorez la valeur de la propriété "CellSpacing".
table.allow_cell_spacing = allow_cell_spacing
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowCellSpacing.html')
# Ajuster la propriété "CellSpacing" activera automatiquement l'espacement des cellules.
table.cell_spacing = 5
self.assertTrue(table.allow_cell_spacing)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

