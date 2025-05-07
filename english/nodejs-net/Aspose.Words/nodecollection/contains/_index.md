---
title: NodeCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Node.js
description: "NodeCollection.contains method. Determines whether a node is in the collection."
type: docs
weight: 50
url: /nodejs-net/aspose.words/nodecollection/contains/
---

## contains(node) {#node}

Determines whether a node is in the collection.


```js
contains(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to locate. |

### Remarks

This method performs a linear search; therefore, the average execution time is proportional to [NodeCollection.count](../count/).




### Returns

``true`` if item is found in the collection; otherwise, ``false``.


### Examples

Shows how to work with a NodeCollection.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add text to the document by inserting Runs using a DocumentBuilder.
builder.write("Run 1. ");
builder.write("Run 2. ");

// Every invocation of the "Write" method creates a new aw.Run,
// which then appears in the parent Paragraph's RunCollection.
let runs = doc.firstSection.body.firstParagraph.runs;

expect(runs.count).toEqual(2);

// We can also insert a node into the RunCollection manually.
let newRun = new aw.Run(doc, "Run 3. ");
runs.insert(3, newRun);

expect(runs.contains(newRun)).toEqual(true);
expect(doc.getText().trim()).toEqual("Run 1. Run 2. Run 3.");

// Access individual runs and remove them to remove their text from the document.
let run = runs.at(1);
runs.remove(run);

expect(doc.getText().trim()).toEqual("Run 1. Run 3.");
expect(run).not.toBe(null);
expect(runs.contains(run)).toEqual(false);
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

