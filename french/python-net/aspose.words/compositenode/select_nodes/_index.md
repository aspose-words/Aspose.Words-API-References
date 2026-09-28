---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /fr/python-net/aspose.words/compositenode/select_nodes/
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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# La NodeList résultant de cette expression XPath contiendra tous les nœuds que nous trouvons à l'intérieur d'un champ.
# Cependant, les nœuds FieldStart et FieldEnd peuvent figurer dans la liste s'il y a des champs imbriqués dans le chemin.
# Actuellement, il ne trouve pas les champs rares dans lesquels le FieldCode ou le FieldResult s'étend sur plusieurs paragraphes.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Vérifiez si le run spécifié est l'un des nœuds qui se trouvent à l'intérieur du champ.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

