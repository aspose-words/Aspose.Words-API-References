---
title: Document.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for Node.js
description: "Document.ensureMinimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 600
url: /nodejs-net/aspose.words/document/ensureMinimum/
---

## ensureMinimum() {#default}

If the document contains no sections, creates one section with one paragraph.


```js
ensureMinimum()
```

### Examples

Shows how to ensure that a document contains the minimal set of nodes required for editing its contents.

```js
// A newly created document contains one child Section, which includes one child Body and one child Paragraph.
// We can edit the document body's contents by adding nodes such as Runs or inline Shapes to that paragraph.
let doc = new aw.Document();
NodeCollection nodes = doc.getChildNodes(aw.NodeType.Any, true);
expect(nodes[0].NodeType).toEqual(aw.NodeType.Section);
expect(nodes[0].ParentNode).toEqual(doc);
expect(nodes[1].NodeType).toEqual(aw.NodeType.Body);
expect(nodes[1].ParentNode).toEqual(nodes[0]);
expect(nodes[2].NodeType).toEqual(aw.NodeType.Paragraph);
expect(nodes[2].ParentNode).toEqual(nodes[1]);
// This is the minimal set of nodes that we need to be able to edit the document.
// We will no longer be able to edit the document if we remove any of them.
doc.removeAllChildren();
expect(doc.getChildNodes(aw.NodeType.Any, true).Count).toEqual(0);
// Call this method to make sure that the document has at least those three nodes so we can edit it again.
doc.ensureMinimum();
expect(nodes[0].NodeType).toEqual(aw.NodeType.Section);
expect(nodes[1].NodeType).toEqual(aw.NodeType.Body);
expect(nodes[2].NodeType).toEqual(aw.NodeType.Paragraph);
((Paragraph)nodes[2]).Runs.add(new aw.Run(doc, "Hello world!"));
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

