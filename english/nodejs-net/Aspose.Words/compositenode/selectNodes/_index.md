---
title: CompositeNode.selectNodes method
linktitle: selectNodes method
articleTitle: selectNodes method
second_title: Aspose.Words for Node.js
description: "CompositeNode.selectNodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 330
url: /nodejs-net/aspose.words/compositenode/selectNodes/
---

## selectNodes(xpath) {#string}

Selects a list of nodes matching the XPath expression.


```js
selectNodes(xpath: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | string | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

A list of nodes matching the XPath query.


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

Shows how to use an XPath expression to test whether a node is inside a field.

```js
let doc = new aw.Document(base.myDir + "Mail merge destination - Northwind employees.docx");

// The NodeList that results from this XPath expression will contain all nodes we find inside a field.
// However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
// Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
let resultList =
  doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]").toArray();

// Check if the specified run is one of the nodes that are inside the field.
console.log(`Contents of the first Run node that's part of a field: ${resultList.find(n => n.nodeType == aw.NodeType.Run).asRun().getText().trim()}`);
```

### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

