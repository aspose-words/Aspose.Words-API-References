---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /sv/python-net/aspose.words/compositenode/select_nodes/
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
# Detta uttryck kommer att extrahera alla styckenoder,
# som är ättlingar till någon tabellnod i dokumentet.
node_list = doc.select_nodes('//Table//Paragraph')
# Iterera genom listan med en enumerator och skriv ut innehållet i varje stycke i varje cell i tabellen.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Detta uttryck kommer att välja alla stycken som är direkta barn till någon Body-nod i dokumentet.
node_list = doc.select_nodes('//Body/Paragraph')
# Vi kan behandla listan som en array.
self.assertEqual(4, len(list(node_list)))
# Använd SelectSingleNode för att välja det första resultatet av samma uttryck som ovan.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# NodeList‑en som resultat av detta XPath‑uttryck kommer att innehålla alla noder vi hittar inuti ett fält.
# Dock kan FieldStart‑ och FieldEnd‑noder finnas i listan om det finns nästlade fält i sökvägen.
# För närvarande hittar den inte sällsynta fält där FieldCode eller FieldResult sträcker sig över flera stycken.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Kontrollera om den angivna körningen är en av noderna som finns i fältet.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

