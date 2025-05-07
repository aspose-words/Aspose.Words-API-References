---
title: NodeCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Node.js
description: "NodeCollection.remove method. Removes the node from the collection and from the document."
type: docs
weight: 80
url: /nodejs-net/aspose.words/nodecollection/remove/
---

## remove(node) {#node}

Removes the node from the collection and from the document.


```js
remove(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to remove. |

### Examples

Shows how to work with a NodeCollection.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add text to the document by inserting Runs using a DocumentBuilder.
builder.write("Run 1. ");
builder.write("Run 2. ");

// Every invocation of the "Write" method creates a new Run,
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

