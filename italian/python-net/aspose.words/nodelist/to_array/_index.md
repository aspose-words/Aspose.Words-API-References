---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /it/python-net/aspose.words/nodelist/to_array/
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
# Questa espressione estrarrà tutti i nodi di paragrafo,
# che sono discendenti di qualsiasi nodo tabella nel documento.
node_list = doc.select_nodes('//Table//Paragraph')
# Itera attraverso l'elenco con un enumeratore e stampa il contenuto di ogni paragrafo in ciascuna cella della tabella.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Questa espressione selezionerà tutti i paragrafi che sono figli diretti di qualsiasi nodo Body nel documento.
node_list = doc.select_nodes('//Body/Paragraph')
# Possiamo trattare l'elenco come un array.
self.assertEqual(4, len(list(node_list)))
# Usa SelectSingleNode per selezionare il primo risultato della stessa espressione di sopra.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

