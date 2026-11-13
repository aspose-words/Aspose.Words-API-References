---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /es/python-net/aspose.words/nodelist/to_array/
---

## to_array() {#default}

Copies all nodes from the collection to a new array of nodes.


```python
def to_array(self):
    ...
```

### Remarks

You should not be adding/removing nodes while iterating over a collection 
of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy 
nodes into a fixed-size array and then iterate over the array.




### Returns

An array of nodes.


### Examples

Shows how to select certain nodes by using an XPath expression.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Esta expresión extraerá todos los nodos de párrafo,
# que son descendientes de cualquier nodo de tabla en el documento.
node_list = doc.select_nodes('//Table//Paragraph')
# Itera a través de la lista con un enumerador e imprime el contenido de cada párrafo en cada celda de la tabla.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Esta expresión seleccionará cualquier párrafo que sea hijo directo de cualquier nodo Body en el documento.
node_list = doc.select_nodes('//Body/Paragraph')
# Podemos tratar la lista como una matriz.
self.assertEqual(4, len(list(node_list)))
# Usa SelectSingleNode para seleccionar el primer resultado de la misma expresión anterior.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

