---
title: CompositeNode.selectSingleNode method
linktitle: selectSingleNode method
articleTitle: selectSingleNode method
second_title: Aspose.Words for NodeJs
description: "CompositeNode.selectSingleNode method. Selects the first [Node](../../node/) that matches the XPath expression."
type: docs
weight: 340
url: /nodejs-net/Aspose.Words/compositenode/selectSingleNode/
---

## selectSingleNode(xpath) {#string}

Selects the first [Node](../../node/) that matches the XPath expression.



```js
selectSingleNode(xpath: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | string | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

The first [Node](../../node/) that matches the XPath query or ``null`` if no matching node is found.


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
* class [CompositeNode](../)

