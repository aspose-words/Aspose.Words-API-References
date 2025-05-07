---
title: NodeCollection.insert method
linktitle: insert method
articleTitle: insert method
second_title: Aspose.Words for Node.js
description: "NodeCollection.insert method. Inserts a node into the collection at the specified index."
type: docs
weight: 70
url: /nodejs-net/aspose.words/nodecollection/insert/
---

## insert(index, node) {#number_node}

Inserts a node into the collection at the specified index.


```js
insert(index: number, node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../node/) | The node to insert. |

### Remarks

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than [NodeCollection.count](../count/), the node is added at the end of the collection.

If the index is negative and its absolute value is greater than [NodeCollection.count](../count/), the node is added at the end of the collection.




If the node being inserted was created from another document, you should use 
[DocumentBase.importNode()](../../documentbase/importNode/#node_boolean_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(NotSupportedException)) | The [NodeCollection](../) is a "deep" collection. |

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

