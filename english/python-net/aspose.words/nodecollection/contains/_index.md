---
title: NodeCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "NodeCollection.contains method. Determines whether a node is in the collection."
type: docs
weight: 50
url: /python-net/aspose.words/nodecollection/contains/
---

## contains(node) {#node}

Determines whether a node is in the collection.


```python
def contains(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) |  |

This method performs a linear search; therefore, the average execution time is proportional to [NodeCollection.count](../count/).




### Returns

``True`` if item is found in the collection; otherwise, ``False``.


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

