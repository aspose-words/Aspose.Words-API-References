---
title: ConditionalStyle.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ConditionalStyle.clear_formatting method. Clears formatting of this conditional style."
type: docs
weight: 100
url: /es/python-net/aspose.words/conditionalstyle/clear_formatting/
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
# Establezca el estilo de tabla para colorear los bordes de la primera fila de la tabla en rojo.
table_style.conditional_styles.first_row.borders.color = aspose.pydrawing.Color.red
# Establezca el estilo de tabla para colorear los bordes de la última fila de la tabla en azul.
table_style.conditional_styles.last_row.borders.color = aspose.pydrawing.Color.blue
# A continuación se presentan dos formas de usar el método "ClearFormatting" para borrar los estilos condicionales.
# 1 -  Borre los estilos condicionales para una parte específica de una tabla:
table_style.conditional_styles[0].clear_formatting()
self.assertEqual(aspose.pydrawing.Color.empty(), table_style.conditional_styles.first_row.borders.color)
# 2 -  Borre los estilos condicionales para toda la tabla:
table_style.conditional_styles.clear_formatting()
self.assertTrue(all([s.borders.color == aspose.pydrawing.Color.empty() for s in table_style.conditional_styles]))
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyle](../)

