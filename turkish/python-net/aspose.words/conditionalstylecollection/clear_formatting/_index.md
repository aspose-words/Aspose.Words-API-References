---
title: ConditionalStyleCollection.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.clear_formatting method. Clears all conditional styles of the table style."
type: docs
weight: 150
url: /tr/python-net/aspose.words/conditionalstylecollection/clear_formatting/
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
# Tablo stilini, tablonun ilk satırının kenarlıklarını kırmızı renkte olacak şekilde ayarlayın.
table_style.conditional_styles.first_row.borders.color = aspose.pydrawing.Color.red
# Tablo stilini, tablonun son satırının kenarlıklarını mavi renkte olacak şekilde ayarlayın.
table_style.conditional_styles.last_row.borders.color = aspose.pydrawing.Color.blue
# Aşağıda, koşullu stilleri temizlemek için "ClearFormatting" yöntemini kullanmanın iki yolu verilmiştir.
# 1 -  Tablonun belirli bir bölümü için koşullu stilleri temizleyin:
table_style.conditional_styles[0].clear_formatting()
self.assertEqual(aspose.pydrawing.Color.empty(), table_style.conditional_styles.first_row.borders.color)
# 2 -  Tüm tablo için koşullu stilleri temizleyin:
table_style.conditional_styles.clear_formatting()
self.assertTrue(all([s.borders.color == aspose.pydrawing.Color.empty() for s in table_style.conditional_styles]))
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

