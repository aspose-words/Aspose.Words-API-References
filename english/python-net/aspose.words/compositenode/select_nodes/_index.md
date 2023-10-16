---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /python-net/aspose.words/compositenode/select_nodes/
---

## select_nodes(xpath) {#str}

Selects a list of nodes matching the XPath expression.


```python
def select_nodes(self, xpath: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | str |  |

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

A list of nodes matching the XPath query.


### Examples

Shows how to select certain nodes by using an XPath expression.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

# This expression will extract all paragraph nodes,
# which are descendants of any table node in the document.
node_list = doc.select_nodes("//Table//Paragraph")

# Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
index = 0

for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1

# This expression will select any paragraphs that are direct children of any Body node in the document.
node_list = doc.select_nodes("//Body/Paragraph")

# We can treat the list as an array.
self.assertEqual(4, len(node_list.to_array()))

# Use "select_single_node" to select the first result of the same expression as above.
node = doc.select_single_node("//Body/Paragraph")

self.assertIsInstance(node.as_paragraph(), aw.Paragraph)
```

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(MY_DIR + "Mail merge destination - Northwind employees.docx")

# The NodeList that results from this XPath expression will contain all nodes we find inside a field.
# However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
# Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
result_list = doc.select_nodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]")

# Check if the specified run is one of the nodes that are inside the field.
for node in result_list:
    if node.node_type == aw.NodeType.RUN:
        print("Contents of the first Run node that's part of a field:", node.get_text().strip())
        break
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

