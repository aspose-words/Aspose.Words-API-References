---
title: ConditionalStyleCollection.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.clear_formatting method. Clears all conditional styles of the table style."
type: docs
weight: 150
url: /it/python-net/aspose.words/conditionalstylecollection/clear_formatting/
---

## clear_formatting() {#default}

Clears all conditional styles of the table style.


```python
def clear_formatting(self):
    ...
```

### Examples

Shows how to reset conditional table styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('First row')
builder.end_row()
builder.insert_cell()
builder.write('Last row')
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table.style = table_style
# Imposta lo stile della tabella per colorare i bordi della prima riga della tabella in rosso.
table_style.conditional_styles.first_row.borders.color = aspose.pydrawing.Color.red
# Imposta lo stile della tabella per colorare i bordi dell'ultima riga della tabella in blu.
table_style.conditional_styles.last_row.borders.color = aspose.pydrawing.Color.blue
# Di seguito sono riportati due modi per utilizzare il metodo "ClearFormatting" per cancellare gli stili condizionali.
# 1 -  Cancella gli stili condizionali per una parte specifica di una tabella:
table_style.conditional_styles[0].clear_formatting()
self.assertEqual(aspose.pydrawing.Color.empty(), table_style.conditional_styles.first_row.borders.color)
# 2 -  Cancella gli stili condizionali per l'intera tabella:
table_style.conditional_styles.clear_formatting()
self.assertTrue(all([s.borders.color == aspose.pydrawing.Color.empty() for s in table_style.conditional_styles]))
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

