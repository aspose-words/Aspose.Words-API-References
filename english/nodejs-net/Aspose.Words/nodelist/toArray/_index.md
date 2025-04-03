---
title: NodeList.toArray method
linktitle: toArray method
articleTitle: toArray method
second_title: Aspose.Words for NodeJs
description: "NodeList.toArray method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /nodejs-net/aspose.words/nodelist/toArray/
---

## toArray() {#default}

Copies all nodes from the collection to a new array of nodes.


```js
toArray()
```

### Remarks

You should not be adding/removing nodes while iterating over a collection 
of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy 
nodes into a fixed-size array and then iterate over the array.




### Returns

An array of nodes.


### Examples

Shows how to select certain nodes by using an XPath expression.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

// This expression will extract all paragraph nodes,
// which are descendants of any table node in the document.
let nodeList = doc.selectNodes("//Table//Paragraph");

// Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
var index = 0;

for (var n of nodeList)
  console.log(`Table paragraph index ${index++}, contents: \"${n.asParagraph().getText().trim()}\"`);

// This expression will select any paragraphs that are direct children of any Body node in the document.
nodeList = doc.selectNodes("//Body/Paragraph");

// We can treat the list as an array.
expect(nodeList.toArray().length).toEqual(4);

// Use SelectSingleNode to select the first result of the same expression as above.
let node = doc.selectSingleNode("//Body/Paragraph");

expect(node.nodeType).toEqual(aw.NodeType.Paragraph);
```

### See Also

* module [Aspose.Words](../../)
* class [NodeList](../)

