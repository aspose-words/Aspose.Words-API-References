---
title: NodeCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for NodeJs
description: "NodeCollection.clear method. Removes all nodes from this collection and from the document."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/nodecollection/clear/
---

## clear() {#default}

Removes all nodes from this collection and from the document.


```js
clear()
```

### Examples

Shows how to remove all sections from a document.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

// This document has one section with a few child nodes containing and displaying all the document's contents.
expect(doc.sections.count).toEqual(1);
expect(doc.sections.at(0).getChildNodes(aw.NodeType.Any, true).count).toEqual(17);
expect(doc.getText().trim()).toEqual("Hello World!\r\rHello Word!\r\r\rHello World!");

// Clear the collection of sections, which will remove all of the document's children.
doc.sections.clear();

expect(doc.getChildNodes(aw.NodeType.Any, true).count).toEqual(0);
expect(doc.getText().trim()).toEqual('');
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

