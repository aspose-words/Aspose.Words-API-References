---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /it/python-net/aspose.words/compositenode/select_nodes/
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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# Il NodeList risultante da questa espressione XPath conterrà tutti i nodi che troviamo all'interno di un campo.
# Tuttavia, i nodi FieldStart e FieldEnd possono comparire nella lista se ci sono campi nidificati nel percorso.
# Attualmente non trova campi rari in cui il FieldCode o il FieldResult si estendono su più paragrafi.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Verifica se il run specificato è uno dei nodi presenti all'interno del campo.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

