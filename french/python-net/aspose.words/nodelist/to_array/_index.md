---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /fr/python-net/aspose.words/nodelist/to_array/
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
# Cette expression extraira tous les nœuds de paragraphe,
# qui sont des descendants de n'importe quel nœud de tableau dans le document.
node_list = doc.select_nodes('//Table//Paragraph')
# Itérez à travers la liste avec un énumérateur et imprimez le contenu de chaque paragraphe dans chaque cellule du tableau.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Cette expression sélectionnera tous les paragraphes qui sont des enfants directs de n'importe quel nœud Body dans le document.
node_list = doc.select_nodes('//Body/Paragraph')
# Nous pouvons traiter la liste comme un tableau.
self.assertEqual(4, len(list(node_list)))
# Utilisez SelectSingleNode pour sélectionner le premier résultat de la même expression que ci‑dessus.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

