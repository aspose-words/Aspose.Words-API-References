---
title: NodeList.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "NodeList.count property. Gets the number of nodes in the list."
type: docs
weight: 20
url: /es/python-net/aspose.words/nodelist/count/
---

## NodeList.count property

Gets the number of nodes in the list.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to use XPaths to navigate a NodeList.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserta algunos nodos con un DocumentBuilder.
builder.writeln('Hello world!')
builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_table()
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Nuestro documento contiene tres nodos Run.
node_list = doc.select_nodes('//Run')
self.assertEqual(3, node_list.count)
self.assertTrue(any([n.get_text().strip() == 'Hello world!' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 1' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 2' for n in node_list]))
# Usa una doble barra diagonal para seleccionar todos los nodos Run
# que son descendientes indirectos de un nodo Table, lo que serían los runs dentro de las dos celdas que insertamos.
node_list = doc.select_nodes('//Table//Run')
self.assertEqual(2, node_list.count)
self.assertTrue(any([n.get_text().strip() == 'Cell 1' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 2' for n in node_list]))
# Las barras diagonales simples especifican relaciones de descendencia directa,
# que omitimos cuando usamos barras dobles.
self.assertEqual(doc.select_nodes('//Table//Run'), doc.select_nodes('//Table/Row/Cell/Paragraph/Run'))
# Accede a la forma que contiene la imagen que insertamos.
node_list = doc.select_nodes('//Shape')
self.assertEqual(1, node_list.count)
shape = node_list[0].as_shape()
self.assertTrue(shape.has_image)
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

