---
title: Node.parentNode property
linktitle: parentNode property
articleTitle: parentNode property
second_title: Aspose.Words for NodeJs
description: "Node.parentNode property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/node/parentNode/
---

## Node.parentNode property

Gets the immediate parent of this node.


```js
get parentNode(): Aspose.Words.CompositeNode
```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``null``.




### Examples

Shows how to access a node's parent node.

```js
let doc = new aw.Document();
let para = doc.firstSection.body.firstParagraph;

// Append a child Run node to the document's first paragraph.
let run = new aw.Run(doc, "Hello world!");
para.appendChild(run);

// The paragraph is the parent node of the run node. We can trace this lineage
// all the way to the document node, which is the root of the document's node tree.
expect(run.parentNode.referenceEquals(para)).toEqual(true);
expect(para.parentNode.referenceEquals(doc.firstSection.body)).toEqual(true);
expect(doc.firstSection.body.parentNode.referenceEquals(doc.firstSection)).toEqual(true);
expect(doc.firstSection.parentNode.referenceEquals(doc)).toEqual(true);
```

Shows how to create a node and set its owning document.

```js
let doc = new aw.Document();
let para = new aw.Paragraph(doc);
para.appendChild(new aw.Run(doc, "Hello world!"));

// We have not yet appended this paragraph as a child to any composite node.
expect(para.parentNode).toBe(null);

// If a node is an appropriate child node type of another composite node,
// we can attach it as a child only if both nodes have the same owner document.
// The owner document is the document we passed to the node's constructor.
// We have not attached this paragraph to the document, so the document does not contain its text.
expect(doc.referenceEquals(para.document)).toEqual(true);
expect(doc.getText().trim()).toEqual('');

// Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
para.paragraphFormat.style = doc.styles.at("Heading 1");

// Add this node to the document, and then verify its contents.
doc.firstSection.body.appendChild(para);

expect(para.parentNode.referenceEquals(doc.firstSection.body)).toEqual(true);
expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

