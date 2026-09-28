---
title: ConditionalStyle.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ConditionalStyle.clear_formatting method. Clears formatting of this conditional style."
type: docs
weight: 100
url: /de/python-net/aspose.words/conditionalstyle/clear_formatting/
---

## clear_formatting() {#default}

Clears formatting of this conditional style.


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
# Legen Sie den Tabellenstil fest, um die Rahmen der ersten Zeile der Tabelle rot zu färben.
table_style.conditional_styles.first_row.borders.color = aspose.pydrawing.Color.red
# Legen Sie den Tabellenstil fest, um die Rahmen der letzten Zeile der Tabelle blau zu färben.
table_style.conditional_styles.last_row.borders.color = aspose.pydrawing.Color.blue
# Unten sind zwei Möglichkeiten zur Verwendung der Methode "ClearFormatting", um die bedingten Formatierungen zu löschen.
# 1 -  Löschen Sie die bedingten Formatierungen für einen bestimmten Teil einer Tabelle:
table_style.conditional_styles[0].clear_formatting()
self.assertEqual(aspose.pydrawing.Color.empty(), table_style.conditional_styles.first_row.borders.color)
# 2 -  Löschen Sie die bedingten Formatierungen für die gesamte Tabelle:
table_style.conditional_styles.clear_formatting()
self.assertTrue(all([s.borders.color == aspose.pydrawing.Color.empty() for s in table_style.conditional_styles]))
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyle](../)

