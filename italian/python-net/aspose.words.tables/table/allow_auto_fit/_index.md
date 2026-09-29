---
title: Table.allow_auto_fit property
linktitle: allow_auto_fit property
articleTitle: allow_auto_fit property
second_title: Aspose.Words for Python
description: "Table.allow_auto_fit property. Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents."
type: docs
weight: 50
url: /it/python-net/aspose.words.tables/table/allow_auto_fit/
---

## Table.allow_auto_fit property

Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.


```python
@property
def allow_auto_fit(self) -> bool:
    ...

@allow_auto_fit.setter
def allow_auto_fit(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.




### Examples

Shows how to enable/disable automatic table cell resizing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(100)
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.end_row()
builder.end_table()
# Imposta la proprietà "AllowAutoFit" su "false" per fare in modo che la tabella mantenga le dimensioni
# di tutte le sue righe e celle, e trunca i contenuti se diventano troppo grandi per adattarsi.
# Imposta la proprietà "AllowAutoFit" su "true" per consentire alla tabella di modificare la larghezza e l'altezza delle sue celle
# per adattare i loro contenuti.
table.allow_auto_fit = allow_auto_fit
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowAutoFitOnTable.html')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)
* method [Table.auto_fit()](../auto_fit/#autofitbehavior)

