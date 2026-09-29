---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /es/python-net/aspose.words/compositenode/select_nodes/
---

## select_nodes(xpath) {#str}

Selects a list of nodes matching the XPath expression.


```python
def select_nodes(self, xpath: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | str | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

A list of nodes matching the XPath query.


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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# La NodeList que resulta de esta expresión XPath contendrá todos los nodos que encontremos dentro de un campo.
# Sin embargo, los nodos FieldStart y FieldEnd pueden estar en la lista si hay campos anidados en la ruta.
# Actualmente no encuentra campos raros en los que el FieldCode o FieldResult se extienden a través de varios párrafos.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Compruebe si el run especificado es uno de los nodos que están dentro del campo.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

