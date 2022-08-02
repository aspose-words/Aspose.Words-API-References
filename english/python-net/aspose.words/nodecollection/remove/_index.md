---
title: remove method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes the node from the collection and from the document."
type: docs
weight: 80
url: /python-net/aspose.words/nodecollection/remove/
---

## remove(node) {#node}

Removes the node from the collection and from the document.


```python
def remove(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) |  |

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

