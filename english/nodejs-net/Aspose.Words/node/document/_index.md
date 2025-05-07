---
title: Node.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Node.js
description: "Node.document property. Gets the document to which this node belongs."
type: docs
weight: 20
url: /nodejs-net/aspose.words/node/document/
---

## Node.document property

Gets the document to which this node belongs.


```js
get document(): Aspose.Words.DocumentBase
```

### Remarks

The node always belongs to a document even if it has just been created
and not yet added to the tree, or if it has been removed from the tree.




### Examples

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

