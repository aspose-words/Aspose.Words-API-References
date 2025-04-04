---
title: NodeCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Node.js
description: "NodeCollection.add method. Adds a node to the end of the collection."
type: docs
weight: 30
url: /nodejs-net/aspose.words/nodecollection/add/
---

## add(node) {#node}

Adds a node to the end of the collection.


```js
add(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to be added to the end of the collection. |

### Remarks

The node is inserted as a child into the node object from which the collection was created.




If the node being inserted was created from another document, you should use 
[DocumentBase.importNode()](../../documentbase/importNode/#node_boolean_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(NotSupportedException)) | The [NodeCollection](../) is a "deep" collection. |

### Examples

Shows how to prepare a new section node for editing.

```js
let doc = new aw.Document();

// A blank document comes with a section, which has a body, which in turn has a paragraph.
// We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
expect(doc.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Section);
expect(doc.sections.at(0).getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Body);
expect(doc.sections.at(0).body.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Paragraph);

// If we add a new section like this, it will not have a body, or any other child nodes.
doc.sections.add(new aw.Section(doc));

expect(doc.sections.at(1).getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc.lastSection.ensureMinimum();

expect(doc.sections.at(1).getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Body);
expect(doc.sections.at(1).body.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Paragraph);

doc.sections.at(0).body.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

