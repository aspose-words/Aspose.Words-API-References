---
title: CompositeNode.select_single_node method
linktitle: select_single_node method
articleTitle: select_single_node method
second_title: Aspose.Words for Python
description: "CompositeNode.select_single_node method. Selects the first [Node](../../node/) that matches the XPath expression."
type: docs
weight: 200
url: /sv/python-net/aspose.words/compositenode/select_single_node/
---

## select_single_node(xpath) {#str}

Selects the first [Node](../../node/) that matches the XPath expression.



```python
def select_single_node(self, xpath: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | str | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

The first [Node](../../node/) that matches the XPath query or ``None`` if no matching node is found.


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

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

