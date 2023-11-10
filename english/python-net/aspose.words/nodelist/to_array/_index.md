---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /python-net/aspose.words/nodelist/to_array/
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

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

