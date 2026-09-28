---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /de/python-net/aspose.words/compositenode/select_nodes/
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
# Dieser Ausdruck extrahiert alle Absatzknoten,
# die Nachkommen eines beliebigen Tabellenknotens im Dokument sind.
node_list = doc.select_nodes('//Table//Paragraph')
# Iterieren Sie mit einem Enumerator durch die Liste und geben Sie den Inhalt jedes Absatzes in jeder Zelle der Tabelle aus.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Dieser Ausdruck wählt alle Absätze aus, die direkte Kinder eines beliebigen Body-Knotens im Dokument sind.
node_list = doc.select_nodes('//Body/Paragraph')
# Wir können die Liste als Array behandeln.
self.assertEqual(4, len(list(node_list)))
# Verwenden Sie SelectSingleNode, um das erste Ergebnis desselben Ausdrucks wie oben auszuwählen.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# Die NodeList, die aus diesem XPath-Ausdruck resultiert, enthält alle Knoten, die wir innerhalb eines Feldes finden.
# Allerdings können FieldStart- und FieldEnd-Knoten in der Liste sein, wenn verschachtelte Felder im Pfad vorhanden sind.
# Derzeit werden seltene Felder, bei denen der FieldCode oder FieldResult über mehrere Absätze hinweg reicht, nicht gefunden.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Prüfen Sie, ob das angegebene Run eines der Knoten ist, die sich innerhalb des Feldes befinden.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

