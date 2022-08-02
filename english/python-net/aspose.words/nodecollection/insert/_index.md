---
title: insert method
second_title: Aspose.Words for Python via .NET API Reference
description: "Inserts a node into the collection at the specified index."
type: docs
weight: 70
url: /python-net/aspose.words/nodecollection/insert/
---

## insert(index, node) {#int_node}

Inserts a node into the collection at the specified index.


```python
def insert(self, index: int, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| node | [Node](../../node/) |  |

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than Count, the node is added at the end of the collection.

If the index is negative and its absolute value is greater than Count, the node is added at the end of the collection.




If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Exceptions

| exception | condition |
| --- | --- |
| System.NotSupportedException | The **NodeCollection** is a "deep" collection. |

### Examples

Shows how to work with a NodeCollection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add text to the document by inserting Runs using a DocumentBuilder.
builder.write("Run 1. ")
builder.write("Run 2. ")

# Every invocation of the "write" method creates a new Run,
# which then appears in the parent Paragraph's RunCollection.
runs = doc.first_section.body.first_paragraph.runs

self.assertEqual(2, runs.count)

# We can also insert a node into the RunCollection manually.
new_run = aw.Run(doc, "Run 3. ")
runs.insert(3, new_run)

self.assertTrue(runs.contains(new_run))
self.assertEqual("Run 1. Run 2. Run 3.", doc.get_text().strip())

# Access individual runs and remove them to remove their text from the document.
run = runs[1]
runs.remove(run)

self.assertEqual("Run 1. Run 3.", doc.get_text().strip())
self.assertIsNotNone(run)
self.assertFalse(runs.contains(run))
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

