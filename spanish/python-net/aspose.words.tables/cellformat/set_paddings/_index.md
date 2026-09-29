---
title: CellFormat.set_paddings method
linktitle: set_paddings method
articleTitle: set_paddings method
second_title: Aspose.Words for Python
description: "CellFormat.set_paddings method. Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell."
type: docs
weight: 170
url: /es/python-net/aspose.words.tables/cellformat/set_paddings/
---

## set_paddings(left_padding, top_padding, right_padding, bottom_padding) {#float_float_float_float}

Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.


```python
def set_paddings(self, left_padding: float, top_padding: float, right_padding: float, bottom_padding: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| left_padding | float |  |
| top_padding | float |  |
| right_padding | float |  |
| bottom_padding | float |  |

### Examples

Shows how to pad the contents of a cell with whitespace.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Establece una distancia de relleno (en puntos) entre el borde y el contenido del texto
# de cada celda de tabla que creamos con el generador de documentos.
builder.cell_format.set_paddings(5, 10, 40, 50)
# Crea una tabla con una celda cuyo contenido tendrá relleno de espacio en blanco.
builder.start_table()
builder.insert_cell()
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.Padding.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

